add_definitions("-DACSDK_LOG_MODULE=bluetooth")

add_library(Bluetooth SHARED Bluetooth.cpp SQLiteBluetoothStorage.cpp)

target_include_directories(Bluetooth PUBLIC
    "${Bluetooth_SOURCE_DIR}/include")

target_link_libraries(
    Bluetooth
    AVSCommon
    SQLiteStorage
)

# install target
asdk_install()
