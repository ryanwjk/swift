add_swift_library(swiftCoreImage ${SWIFT_SDK_OVERLAY_LIBRARY_BUILD_TYPES} IS_SDK_OVERLAY
  CoreImage.swift

  SWIFT_COMPILE_FLAGS "${SWIFT_RUNTIME_SWIFT_COMPILE_FLAGS}"
  LINK_FLAGS "${SWIFT_RUNTIME_SWIFT_LINK_FLAGS}"
  TARGET_SDKS OSX IOS IOS_SIMULATOR TVOS TVOS_SIMULATOR
  SWIFT_MODULE_DEPENDS_OSX Darwin CoreGraphics Dispatch Foundation IOKit ObjectiveC XPC # auto-updated
  SWIFT_MODULE_DEPENDS_IOS Darwin CoreGraphics Dispatch Foundation ObjectiveC # auto-updated
  SWIFT_MODULE_DEPENDS_TVOS Darwin CoreGraphics Dispatch Foundation ObjectiveC # auto-updated
  FRAMEWORK_DEPENDS_OSX QuartzCore
  FRAMEWORK_DEPENDS_IOS_TVOS CoreImage
)
