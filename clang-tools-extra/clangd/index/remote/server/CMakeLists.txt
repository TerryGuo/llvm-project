set(LLVM_LINK_COMPONENTS
  LineEditor
  Support
  )
add_clang_executable(clangd-index-server
  Server.cpp
  )
target_link_libraries(clangd-index-server
  PRIVATE
  clangDaemon

  RemoteIndexProtos
  clangdRemoteMarshalling

  grpc++
  )
