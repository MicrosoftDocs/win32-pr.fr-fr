---
description: Interfaces (Windows Runtime C++)
ms.assetid: CB05B5F8-BE15-4BE0-A651-F6E8912D649D
title: Interfaces (Windows Runtime)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f627a77f91417b16d8bfc3e940036910003c40f0
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106543380"
---
# <a name="interfaces"></a>Interfaces

## <a name="in-this-section"></a>Dans cette section

| Interface | Description |
|-|-|
| [**IActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iactivatableclassregistration) | Active l’obtention des informations d’inscription pour une classe. |
| [**IActivationFactory**](/windows/win32/api/activation/nn-activation-iactivationfactory) | Permet aux classes d'être activées par le Windows Runtime. |
| [**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference) | Permet de récupérer une référence agile à un objet. |
| [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) | Active l’inscription d’un gestionnaire de notification d’arrêt cloisonné. |
| [**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md) | Représente la méthode qui est appelée lorsqu’une action asynchrone se termine. |
| [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) | Représente une opération asynchrone. |
| [**IAsyncActionProgressHandler<TProgress>**](/previous-versions//br205782(v=vs.85)) | Représente la méthode qui est appelée lorsqu’une action asynchrone signale la progression. |
| [**IAsyncActionWithProgress<TProgress>**](/previous-versions//br205784(v=vs.85)) | Représente une action asynchrone qui rapporte la progression. |
| [**IAsyncActionWithProgressCompletedHandler<TProgress>**](/previous-versions//br205785(v=vs.85)) | Représente la méthode qui est appelée lorsqu’une action asynchrone qui signale la progression se termine. |
| [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo) | Prend en charge les opérations asynchrones. |
| [**IAsyncOperation<TResult>**](/previous-versions//br205802(v=vs.85)) | Représente une opération asynchrone qui retourne une valeur. |
| [**IAsyncOperationCompletedHandler<TResult>**](/previous-versions//br205803(v=vs.85)) | Représente la méthode qui est appelée lorsqu’une opération asynchrone se termine. |
| [**IAsyncOperationProgressHandler**](/previous-versions//br205805(v=vs.85)) | Représente la méthode qui est appelée lorsqu’une opération asynchrone signale la progression. |
| [**IAsyncOperationWithProgress**](/previous-versions//br205807(v=vs.85)) | Représente une opération asynchrone qui retourne un résultat et signale une progression. |
| [**IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>**](/previous-versions//br205808(v=vs.85)) | Représente la méthode qui est appelée lorsqu’une opération asynchrone qui signale la progression se termine. |
| [**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative) | Représente un cadre de données audio. |
| [**IAudioFrameNativeFactory**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenativefactory) | Crée des instances de [**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative). |
| [**IBuffer**](/previous-versions//hh438362(v=vs.85)) | Représente un tableau d’octets. |
| [**IBufferByteAccess**](/previous-versions//hh846267(v=vs.85)) | Représente une mémoire tampon sous la forme d’un tableau d’octets. |
| [**IClosable**](/windows/win32/api/windows.foundation/nn-windows-foundation-iclosable) | Définit une méthode pour libérer des ressources allouées. |
| [**ICompositionDrawingSurfaceInterop**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop) | Interface d’interopérabilité native qui autorise le dessin sur un objet surface à l’aide d’un RECT pour définir la zone dans laquelle dessiner. |
| [**ICompositionDrawingSurfaceInterop2**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop2) | Interface d’interopérabilité native qui vous permet de lire le contenu d’une surface de dessin de composition (ou d’une surface de dessin virtuelle de composition). |
| [**ICompositionGraphicsDeviceInterop**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiongraphicsdeviceinterop) | Interface d’interopérabilité native qui permet d’obtenir et de définir le périphérique graphique. |
| [**IContactManagerInterop**](/previous-versions//dn302109(v=vs.85)) | Permet d’accéder aux méthodes [**ContactManager**](/uwp/api/Windows.ApplicationModel.Contacts.ContactManager?view=winrt-19041) dans une application qui gère plusieurs fenêtres. |
| [**ICoreApplication**](/previous-versions//hh438365(v=vs.85)) | Permet aux applications de gérer les modifications d’État, de gérer les fenêtres et de les intégrer à divers frameworks d’interface utilisateur. |
| [**ICoreApplicationExit**](/previous-versions//hh438366(v=vs.85)) | Permet d’arrêter l’exécution des applications du Windows Store. |
| [**ICoreApplicationInitialization**](/previous-versions//hh438370(v=vs.85)) | Contient une méthode Run qui est utilisée pour démarrer l’objet application à partir du point d’entrée d’une application. |
| [**ICoreApplicationView**](/previous-versions//hh438372(v=vs.85)) | Représente une vue d’une application. |
| [**ICoreImmersiveApplication**](/previous-versions//hh438382(v=vs.85)) | Contient des méthodes pour gérer des vues dans une application. |
| [**ICoreInputInterop**](/windows/desktop/api/corewindow/nn-corewindow-icoreinputinterop) | Active une source d’entrée sur l’objet [**CoreInput**](https://www.bing.com/search?q=**CoreInput**) d’une application du Windows Store. |
| [**ICoreWindowInterop**](/windows/desktop/api/corewindow/nn-corewindow-icorewindowinterop) | Permet aux applications d’obtenir la fenêtre handleof la fenêtre ([**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041)) associée à cette interface. |
| [**IDllServerActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-idllserveractivatableclassregistration) | Permet d’obtenir les informations d’inscription d’un serveur in-process. |
| [**IErrorReportingSettings**](/previous-versions//br205818(v=vs.85)) | Fournit l’intégration du débogueur pour les applications Windows Runtime. |
| [**IEventHandler<T>**](/previous-versions//hh438385(v=vs.85)) | Représente la méthode qui gérera un événement qui a des données d’événement de type **T**. |
| [**IExeServerActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration) | Permet d’obtenir les informations d’inscription d’un serveur hors processus. |
| [**IExeServerRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iexeserverregistration) | Représente un serveur hors processus inscrit. |
| [**IFindReferenceTargetsCallback**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ifindreferencetargetscallback) | Définit l’interface pour les rappels à partir de [**IReferenceTracker :: FindTrackerTargets**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-findtrackertargets). L’implémentation de cette interface doit passer toutes les instances [**IReferenceTrackerTarget**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget) qu’elle trouve à la méthode **FoundTrackerTarget** . |
| [**IInputPaneInterop**](/windows/desktop/api/inputpaneinterop/nn-inputpaneinterop-iinputpaneinterop) | Permet l’accès aux membres de la classe [**InputPane**](/uwp/api/Windows.UI.ViewManagement.InputPane?view=winrt-19041) dans une application de bureau. |
| [**IInputStream**](/previous-versions//hh438387(v=vs.85)) | Permet d’obtenir une opération de lecture asynchrone sur un flux séquentiel d’octets. |
| [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable) | Fournit les fonctionnalités requises pour toutes les classes Windows Runtime. |
| [**IIterable<T>**](/previous-versions//br205825(v=vs.85)) | Expose l’itérateur, qui prend en charge une itération simple sur une collection d’un type spécifié. |
| [**IIterator<T>**](/previous-versions//br205827(v=vs.85)) | Prend en charge l’itération sur une collection. |
| [**IKeyValuePair<K, V>**](/previous-versions//br205831(v=vs.85)) | Représente une paire clé-valeur. |
| [**ILanguageExceptionErrorInfo**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo) | Permet de récupérer le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) stocké dans les informations d’erreur avec l’appel à RoOriginateLanguageException. |
| [**ILanguageExceptionErrorInfo2**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo2) | Permet aux projections de langage de fournir et de récupérer les informations d’erreur comme avec [**ILanguageExceptionErrorInfo**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo), avec l’avantage supplémentaire de travailler au-delà des limites du langage. |
| [**ILanguageExceptionTransform**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptiontransform) | Permet aux projections de langage de mettre à la disposition du système tout ou partie du contexte d’une exception qui est levée à partir du contexte d’un gestionnaire catch qui intercepte une exception différente. |
| [**ILanguageExceptionStackBackTrace**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionstackbacktrace) | Permet aux projections de fournir une trace de la pile personnalisée pour cette exception. |
| [**IMap<K, V>**](/previous-versions//br205834(v=vs.85)) | Représente une collection associative. |
| [**IMapChangedEventArgs<K>**](/previous-versions//br205835(v=vs.85)) | Fournit des données pour un événement [**MapChanged**](/uwp/api/windows.foundation.collections.iobservablemap-2?view=winrt-19041) . |
| [**IMapView<K, V>**](/previous-versions//br205838(v=vs.85)) | Représente une vue immuable dans un [**IMap (K, V)**](/previous-versions//br205834(v=vs.85)). |
| [**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85)) | Fournit l’accès à un [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) sous la forme d’un tableau d’octets. |
| [**IMetaDataAssemblyImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport) | Fournit des méthodes pour accéder au contenu d'un manifeste d'assembly et l'examiner. |
| [**IMetaDataDispenser**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenser) | Fournit des méthodes pour créer une portée de métadonnées ou en ouvrir une existante. |
| [**IMetaDataDispenserEx**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenserex) | Étend l’interface [**IMetaDataDispenser**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenser) pour offrir la possibilité de contrôler la manière dont les API de métadonnées fonctionnent sur la portée de métadonnées actuelle. |
| [**IMetaDataImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport) | Fournit des méthodes pour importer et manipuler les métadonnées existantes à partir d'un fichier exécutable portable (PE) ou d'une autre source, comme une bibliothèque de types ou un fichier binaire de métadonnées autonome au moment de l'exécution. |
| [**IMetaDataImport2**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport2) | Étend l’interface [**IMetaDataImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport) pour offrir la possibilité d’utiliser des types génériques. |
| [**IMetaDataTables**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables) | Fournit des méthodes pour le stockage et la récupération d'informations de métadonnées dans des tables. |
| [**IMetaDataTables2**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables2) | Étend [**IMetaDataTables**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables) pour inclure des méthodes permettant d’utiliser des flux de métadonnées. |
| [**IObservableMap<K, V>**](/previous-versions//br205851(v=vs.85)) | Notifie les gestionnaires d’événements des modifications dynamiques apportées à un mappage, par exemple lorsque des éléments sont ajoutés ou supprimés. |
| [**IObservableVector<T>**](/previous-versions//br205854(v=vs.85)) | Avertit les gestionnaires d’événements des modifications apportées au vecteur. |
| [**IOplockBreakingHandler**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-ioplockbreakinghandler) | Cette interface n’est pas implémentée actuellement. |
| [**IOutputStream**](/previous-versions//hh438390(v=vs.85)) | Permet d’obtenir une opération d’écriture asynchrone sur un flux séquentiel d’octets. |
| [**IPdfRendererNative**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) | Représente une API hautes performances permettant d’afficher une seule page d’un fichier PDF (portable document format). |
| [**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85)) | Permet aux développeurs du débogueur de contrôler le cycle de vie d’une application du Windows Store, par exemple lorsqu’elle est suspendue ou reprise. |
| [**IPlayToManagerInterop**](/windows/desktop/api/playtomanagerinterop/nn-playtomanagerinterop-iplaytomanagerinterop) | Permet d’accéder aux méthodes [**PlayToManager**](/uwp/api/Windows.Media.PlayTo.PlayToManager?view=winrt-19041) dans une application du Windows Store qui gère plusieurs fenêtres. |
| [**IPrintManagerInterop**](/windows/desktop/api/printmanagerinterop/nn-printmanagerinterop-iprintmanagerinterop) | Permet d’accéder aux méthodes [**PrintManager**](/uwp/api/Windows.Graphics.Printing.PrintManager?view=winrt-19041) dans une application du Windows Store qui gère plusieurs fenêtres. |
| [**IPropertyValue**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvalue) | Représente une valeur dans un magasin de propriétés Windows Runtime. |
| [**IPropertyValueStatics**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics) | Crée les objets [**IPropertyValue**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvalue) que vous pouvez stocker dans une banque de propriétés. |
| [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) | Permet d’obtenir un lecteur d’octets asynchrone ou un writer d’octet positionné à l’emplacement spécifié sur un flux d’octets d’accès aléatoire. |
| [**IRandomAccessStreamFileAccessMode**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-irandomaccessstreamfileaccessmode) | Fournit l’accès au mode d’accès aux fichiers utilisé lors de l’appel de la méthode [**StorageFile. OpenAsync**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) pour ouvrir le flux d’octets à accès aléatoire. |
| [**IReference<T>**](/previous-versions//br224583(v=vs.85)) | Permet d’étendre le système de propriétés Windows Runtime pour les énumérations définies par l’utilisateur, les structures et les types délégués. |
| [**IReferenceArray<T>**](/previous-versions//br224584(v=vs.85)) | Permet d’étendre le système de propriétés Windows Runtime pour les tableaux d’énumérations définies par l’utilisateur, de structures et de types délégués. |
| [**IReferenceTracker**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker) | Définit l’interface implémentée par l’infrastructure XAML pour la gestion des références d’objet XAML. |
| [**IReferenceTrackerHost**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost) | Définit une interface qui fournit les services globaux utilisés par le système de garbage collection (GC) utilisé par l’infrastructure XAML. |
| [**IReferenceTrackerManager**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager) | Définit l’interface pour un gestionnaire de références d’objet XAML. Implémentez cette interface pour gérer des instances de [**IReferenceTracker**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker) sur des objets XAML. |
| [**IReferenceTrackerTarget**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget) | Définit une interface implémentée par un objet garbage collector référencé à partir de XAML. |
| [**IRestrictedErrorInfo**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) | Représente les détails d’une erreur, y compris les informations d’erreur restreintes. |
| [**ISoftwareBitmapNative**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative) | Représente une image bitmap logicielle. |
| [**ISoftwareBitmapNativeFactory**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnativefactory) | Crée des instances de [**ISoftwareBitmapNative**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative). |
| [**IStorageFolderHandleAccess**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istoragefolderhandleaccess) | Permet d’accéder au handle du système d’exploitation d’un dossier de stockage. |
| [**IStorageItemHandleAccess**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istorageitemhandleaccess) | Permet d’accéder au handle du système d’exploitation d’un fichier de stockage. |
| [**IStringable**](/windows/win32/api/windows.foundation/nn-windows-foundation-istringable) | Fournit un moyen de représenter l’objet actuel sous forme de chaîne. |
| [**ISurfaceImageSourceManagerNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcemanagernative) | Permet d’effectuer des opérations en bloc sur tous les objets [**SurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.SurfaceImageSource?view=winrt-19041) créés dans le même processus. |
| [**ISurfaceImageSourceNativeWithD2D**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d) | Fournit l’implémentation d’une surface Microsoft DirectX partagée qui est affichée dans un [**SurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.SurfaceImageSource?view=winrt-19041) ou un [**VirtualSurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.VirtualSurfaceImageSource?view=winrt-19041). |
| [**ISurfaceImageSourceNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative) | Fournit l’implémentation d’une surface partagée de taille fixe pour le dessin Direct2D. |
| [**ISuspendingDeferral**](isuspendingdeferral.md) | Gère une opération d’interruption d’application retardée. |
| [**ISuspendingEventArgs**](isuspendingeventargs.md) | Fournit des données pour un événement d’interruption de l’application. |
| [**ISuspendingOperation**](isuspendingoperation.md) | Fournit des informations sur une opération d’interruption de l’application. |
| [**ISwapChainBackgroundPanelNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative) | Fournit l’interopérabilité entre XAML et une chaîne de permutation DirectX. |
| [**ISwapChainPanelNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative) | Fournit l’interopérabilité entre XAML et une chaîne de permutation DirectX. Contrairement à [**SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel?view=winrt-19041), un **SwapChainPanel** peut apparaître à n’importe quel niveau de l’arborescence d’affichage XAML, et plus de 1 peuvent être présents dans une arborescence donnée. |
| [**ISwapChainPanelNative2**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative2) | Fournit l’interopérabilité entre XAML et une chaîne de permutation DirectX. Contrairement à [**SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel?view=winrt-19041), un **SwapChainPanel** peut apparaître à n’importe quel niveau de l’arborescence d’affichage XAML, et plus de 1 peuvent être présents dans une arborescence donnée. |
| [**ITypedEventHandler<TSender, TArgs>**](/previous-versions//hh438424(v=vs.85)) | Représente la méthode qui gérera un événement à partir d’un expéditeur de type **TSender** et des données d’événement de type **T**. |
| [**IUnbufferedFileHandleOplockCallback**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleoplockcallback) | Définit une méthode de rappel que vous souhaitez exécuter lorsque le verrou opportuniste pour un handle obtenu en appelant la méthode [**IUnbufferedFileHandleProvider :: OpenUnbufferedFileHandle**](/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle) est rompu. |
| [**IUnbufferedFileHandleProvider**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleprovider) | Fournit l’accès aux descripteurs à partir d’un flux d’octets à accès aléatoire créé par la méthode [**StorageFile. OpenAsync**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) . |
| [**IVector<T>**](/previous-versions//br224590(v=vs.85)) | Représente une collection d’éléments à accès aléatoire. |
| [**IVectorChangedEventArgs**](ivectorchangedeventargs.md) | Fournit des données pour un événement [**VectorChanged**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) . |
| [**IVectorView<T>**](/previous-versions//br224594(v=vs.85)) | Représente une vue immuable dans un [**IVector (T)**](/uwp/api/windows.foundation.collections.ivector-1?view=winrt-19041). |
| [**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative) | Représente un frame de données vidéo. |
| [**IVideoFrameNativeFactory**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenativefactory) | Crée des instances de [**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative). |
| [**IViewProvider**](/previous-versions//hh438426(v=vs.85)) | Représente une vue dans une application. |
| [**IViewProviderFactory**](/previous-versions//hh438427(v=vs.85)) | Crée une instance des vues qui implémentent l’interface [**IViewProvider**](/previous-versions//hh438426(v=vs.85)) . |
| [**IVirtualSurfaceImageSourceNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative) | Fournit l’implémentation d’une surface partagée de grande taille (supérieure à celle de l’écran) pour le dessin DirectX. |
| [**IVirtualSurfaceUpdatesCallbackNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceupdatescallbacknative) | Fournit une interface pour l’implémentation de comportements de dessin lorsqu’un [**VirtualSurfaceImageSource**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative) demande une mise à jour. |
| [**IWeakReference**](/windows/win32/api/weakreference/nn-weakreference-iweakreference) | Représente une référence faible à un objet. |
| [**IWeakReferenceSource**](/windows/win32/api/weakreference/nn-weakreference-iweakreferencesource) | Représente un objet source dans lequel une référence faible peut être récupérée. |
| [**MapChangedEventHandler<K, V>**](/previous-versions//br224612(v=vs.85)) | Représente la méthode qui gère l’événement [**MapChanged**](/uwp/api/windows.foundation.collections.iobservablemap-2?view=winrt-19041) d’un mappage observable. |
| [**VectorChangedEventHandler<T>**](/previous-versions//br224626(v=vs.85)) | Représente la méthode qui gère l’événement [**VectorChanged**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) d’un vecteur observable. |
