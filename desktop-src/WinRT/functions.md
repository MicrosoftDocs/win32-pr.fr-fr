---
description: référence pour les fonctions Windows Runtime C++.
ms.assetid: 3D60C81F-B1CC-4485-B7C3-B1C6E903865B
title: fonctions (Windows Runtime)
ms.topic: article
ms.date: 05/10/2019
ms.openlocfilehash: fbf0d4ce350251e1c13d1f6a3ff03c95068558098eac722979bc77499a094c4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795009"
---
# <a name="functions-windows-runtime-c-reference"></a>functions (référence C++ Windows Runtime)

## <a name="in-this-section"></a>Dans cette section



| Fonction | Description |
|-|-|
| [**CoDecodeProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-codecodeproxy) | Localise l’implémentation d’une interface COM (Component Object Model) dans un processus serveur en fonction d’une interface vers un objet proxy. |
| [**CreateControlInput**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinput) | Crée un objet [**ICoreInputSourceBase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) dans le thread d’interface utilisateur de l’appelant. |
| [**CreateControlInputEx**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinputex) | Crée un objet [**ICoreInputSourceBase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) dans un thread de travail ou le thread d’interface utilisateur.  |
| [**CreateDirect3D11DeviceFromDXGIDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11devicefromdxgidevice) | Crée une instance de IDirect3DDevice à partir d’un IDXGIDevice. |
| [**CreateDirect3D11SurfaceFromDXGISurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11surfacefromdxgisurface) | Crée une instance de IDirect3DSurface à partir d’un IDXGISurface. |
| [**CreateDirect3DDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3ddevice) | Crée une instance de [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) à partir d’un [IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice). |
| [**CreateDirect3DSurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3dsurface) | Crée une instance de [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) à partir d’un [IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface). |
| [**CreateRandomAccessStreamOnFile**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamonfile) | crée un flux d’accès aléatoire Windows Runtime pour un fichier. |
| [**CreateRandomAccessStreamOverStream**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamoverstream) | crée un flux d’accès aléatoire Windows Runtime autour d’une implémentation de base [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . |
| [**CreateStreamOverRandomAccessStream**](/windows/win32/api/shcore/nf-shcore-createstreamoverrandomaccessstream) | crée un [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) autour d’un objet Windows Runtime [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) . |
| [**CreateXamlUIPresenter**](createxamluipresenter.md) | Fonction de créateur statique qui peut créer un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) pour une surface de rendu dans une application de bureau. |
| [**DbgRaiseAssertionFailure**](/previous-versions//jj635749(v=vs.85)) | Déclenche une assertion pour le débogage.  |
| [**GetDXGIInterface (IDirect3DDevice ^, DXGI_TYPE**) * *](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface) | Récupère une interface DXGI à partir d’une instance [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) . |
| [**GetDXGIInterface (IDirect3DSurface ^, DXGI_TYPE**) * *](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface-r1) | Récupère une interface DXGI à partir d’une instance [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) . |
| [**GetDXGIInterfaceFromObject**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterfacefromobject) | Récupère une interface DXGI à partir d’un objet. |
| [**GetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-getrestrictederrorinfo) | Obtient l’objet d’informations d’erreur restreint défini par un appel précédent à [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) dans le thread logique actuel. |
| [**HSTRING \_ UserFree**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree) | Libère les ressources côté serveur quand elles sont appelées par des fichiers stub RPC. |
| [**HSTRING \_ UserFree64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree64) | Libère les ressources côté serveur quand elles sont appelées par des fichiers stub RPC.  |
| [**HSTRING \_ UserMarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal) | Marshale un objet [**HSTRING**](hstring.md) dans la mémoire tampon RPC. |
| [**HSTRING \_ UserMarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal64) | Marshale un objet [**HSTRING**](hstring.md) dans la mémoire tampon RPC. |
| [**HSTRING \_ utilisateurs**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize) | Calcule la taille du câble de l’objet [**HSTRING**](hstring.md) et obtient son handle et ses données. |
| [**HSTRING \_ UserSize64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize64) | Calcule la taille du câble de l’objet [**HSTRING**](hstring.md) et obtient son handle et ses données. |
| [**HSTRING \_ UserUnmarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal) | Démarshale un objet [**HSTRING**](hstring.md) de la mémoire tampon RPC. |
| [**HSTRING \_ UserUnmarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal64) | Démarshale un objet [**HSTRING**](hstring.md) de la mémoire tampon RPC. |
| [**IsErrorPropagationEnabled**](/windows/win32/api/roerrorapi/nf-roerrorapi-iserrorpropagationenabled) | indique si l’événement [**CoreApplication. UnhandledErrorDetected**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) se produit pour les erreurs retournées par le délégué enregistré en tant que fonction de rappel pour un événement d’API Windows Runtime ou l’achèvement d’une méthode asynchrone. |
| [**DllGetActivationFactory**](/previous-versions//br205771(v=vs.85)) | récupère la fabrique d’activation à partir d’une DLL qui contient des classes d’Windows Runtime activables. |
| [**MetaDataGetDispenser**](/windows/win32/api/rometadata/nf-rometadata-metadatagetdispenser) | Crée une classe de distributeur. |
| [**PdfCreateRenderer**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfcreaterenderer) | Obtient une instance de l’interface [**IPdfRendererNative**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) pour afficher une seule page d’un fichier PDF (portable document format). |
| [**PdfRenderParams**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfrenderparams) | Remplit un structure [**de \_ \_ paramètres de rendu PDF**](/windows/desktop/api/windows.data.pdf.interop/ns-windows-data-pdf-interop-pdf_render_params) . Une \_ structure de paramètres de rendu PDF \_ représente un ensemble de propriétés pour la génération d’une seule page d’un fichier PDF. |
| [**RoActivateInstance**](/windows/win32/api/roapi/nf-roapi-roactivateinstance) | active la classe de Windows Runtime spécifiée. |
| [**RoCaptureErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext) | Enregistre le contexte d’erreur actuel afin qu’il soit disponible pour des appels ultérieurs à la fonction [**RoFailFastWithErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) . |
| [**RoClearError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roclearerror) | Supprime les informations d’erreur existantes du bloc d’environnement de thread actuel (TEB). |
| [**RoFailFastWithErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) | Déclenche une exception non continuable dans le processus en cours. |
| [**RoFailFastWithErrorContextInternal2**](./roerrorapi/nf-roerrorapi-rofailfastwitherrorcontextinternal2.md) | Déclenche une exception non continuable dans le processus en cours et vous permet également d’inclure un contexte d’erreur supplémentaire qui n’a pas déjà été capturé par le système d’exploitation. |
| [**RoFreeParameterizedTypeExtra**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rofreeparameterizedtypeextra) | Libère le handle alloué par [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid). |
| [**RoGetActivatableClassRegistration**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration) | Permet de récupérer les informations d’inscription de la classe. |
| [**RoGetActivationFactory**](/windows/win32/api/roapi/nf-roapi-rogetactivationfactory) | Obtient la fabrique d’activation pour la classe d’exécution spécifiée. |
| [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) | Crée une référence agile pour un objet spécifié par l’interface donnée. |
| [**RoGetApartmentIdentifier**](/windows/win32/api/roapi/nf-roapi-rogetapartmentidentifier) | Obtient un identificateur unique pour le cloisonnement actuel. |
| [**RoGetBufferMarshaler**](/windows/win32/api/robuffer/nf-robuffer-rogetbuffermarshaler) | Fournit un marshaleur IBuffer standard pour implémenter la sémantique associée à l’interface IBuffer lorsqu’il est marshalé. |
| [**RoGetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags) | obtient le comportement de création de rapports actuel des fonctions d’erreur Windows Runtime. |
| [**RoGetMetaDataFile**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-rogetmetadatafile) | Localise et récupère le fichier de métadonnées qui décrit l’interface binaire d’application (ABI) pour le TypeName spécifié. |
| [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) | Calcule l’identificateur d’interface (IID) de l’interface ou du type délégué qui résulte lorsqu’une interface paramétrable ou un délégué est instancié avec les arguments de type spécifiés. |
| [**RoGetServerActivatableClasses**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetserveractivatableclasses) | Récupère les classes activables inscrites pour un serveur exécutable (EXE) donné, inscrit sous l’ID de package du processus appelant. |
| [**RoInitialize**](/windows/win32/api/roapi/nf-roapi-roinitialize) | initialise le Windows Runtime sur le thread en cours avec le modèle d’accès concurrentiel spécifié. |
| [**RoInspectThreadErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectthreaderrorinfo) | Obtient l’objet d’erreur qui représente la pile des appels au point d’origine de l’erreur. |
| [**RoInspectCapturedStackBackTrace**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace) | Permet aux débogueurs d’inspecter une pile des appels à partir d’un processus cible. |
| [**RoOriginateError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerror) | Signale une erreur et une chaîne informatif à un débogueur attaché. |
| [**RoOriginateErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerrorw) | Signale une erreur et une chaîne informatif à un débogueur attaché. |
| [**RoOriginateLanguageException**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginatelanguageexception) | Signale une erreur, une chaîne informatif et un objet d’erreur à un débogueur attaché. |
| [**RoParameterizedTypeExtraGetTypeSignature**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-roparameterizedtypeextragettypesignature) | Obtient la signature de type utilisée pour calculer l’IID à partir du dernier appel à [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) avec le handle spécifié. |
| [**RoParseTypeName**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roparsetypename) | Analyse un nom de type et des paramètres de type existants, dans le cas de types paramétrables. |
| [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) | inscrit un tableau des fabriques d’activation hors processus pour un serveur Windows Runtime exe. |
| [**RoRegisterForApartmentShutdown**](/windows/win32/api/roapi/nf-roapi-roregisterforapartmentshutdown) | Inscrit un rappel [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) à appeler lorsque le cloisonnement actuel s’arrête. |
| [**RoReportUnhandledError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportunhandlederror) | Déclenche le gestionnaire d’erreurs globales lorsqu’une exception non gérée se produit. |
| [**RoReportFailedDelegate**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportfaileddelegate) | Déclenche le gestionnaire d’erreurs globales en cas d’échec d’un délégué. |
| [**RoResolveNamespace**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roresolvenamespace) | déterminez les enfants directs, les types et les sous-espaces de noms de l’espace de noms Windows Runtime spécifié, à partir de n’importe quel langage de programmation pris en charge par l’Windows Runtime. |
| [**RoResolveRestrictedErrorInfoReference**](/windows/win32/api/roerrorapi/nf-roerrorapi-roresolverestrictederrorinforeference) | Retourne le pointeur d’interface [**IRestrictedErrorInfo**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) en fonction de la référence donnée. |
| [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) | supprime du Windows Runtime un tableau de fabriques d’activation inscrites. |
| [**RoSetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags) | définit le comportement de création de rapports des fonctions d’erreur Windows Runtime. |
| [**RoTransformError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerror) | Signale une erreur modifiée et une chaîne informatif à un débogueur attaché. |
| [**RoTransformErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerrorw) | Signale une erreur transformée et une chaîne informatif à un débogueur attaché. |
| [**RoUninitialize**](/windows/win32/api/roapi/nf-roapi-rouninitialize) | ferme la Windows Runtime sur le thread actuel. |
| [**RoUnregisterForApartmentShutdown**](/windows/win32/api/roapi/nf-roapi-rounregisterforapartmentshutdown) | Annule l’inscription d’une interface [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) précédemment inscrite. |
| [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) | Définit l’objet d’informations d’erreur restreint pour le thread actuel. |
| [**WindowsCompareStringOrdinal**](/windows/win32/api/winstring/nf-winstring-windowscomparestringordinal) | Compare deux objets [**HSTRING**](hstring.md) spécifiés et retourne un entier qui indique leur position relative dans un ordre de tri. |
| [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) | Concatène deux chaînes spécifiées. |
| [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) | Crée un [**HSTRING**](hstring.md) en fonction de la chaîne source spécifiée. |
| [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) | Crée une référence de chaîne basée sur la chaîne spécifiée. |
| [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) | Décrémente le décompte de références d’une mémoire tampon de chaîne. |
| [**WindowsDeleteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowsdeletestringbuffer) | Ignore une mémoire tampon de chaîne préallouée si elle n’a pas été promue en [**HSTRING**](hstring.md). |
| [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) | Crée une copie de la chaîne spécifiée. |
| [**WindowsGetStringLen**](/windows/win32/api/winstring/nf-winstring-windowsgetstringlen) | Obtient la longueur, en caractères Unicode, de la chaîne spécifiée. |
| [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) | Obtient la mémoire tampon de stockage pour la chaîne spécifiée. |
| [**WindowsInspectString**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring) | permet aux débogueurs d’afficher la valeur d’un Windows Runtime [**HSTRING**](hstring.md) dans un autre espace d’adressage, à distance ou à partir d’un dump.  |
| [**WindowsInspectString2**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring2) | permet aux débogueurs d’afficher la valeur d’un Windows Runtime [**HSTRING**](hstring.md) dans un autre espace d’adressage, à distance ou à partir d’un dump.  |
| [**WindowsIsStringEmpty**](/windows/win32/api/winstring/nf-winstring-windowsisstringempty) | Indique si la chaîne spécifiée est une chaîne vide. |
| [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) | Alloue une mémoire tampon de caractères mutable pour une utilisation dans la création de [**HSTRING**](hstring.md) . |
| [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) | Crée un [**HSTRING**](hstring.md) à partir de [**la \_ mémoire tampon HSTRING**](hstring-buffer.md)spécifiée. |
| [**WindowsReplaceString**](/windows/win32/api/winstring/nf-winstring-windowsreplacestring) | Remplace toutes les occurrences d’un jeu de caractères dans la chaîne spécifiée par un autre jeu de caractères pour créer une nouvelle chaîne. |
| [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) | Indique si la chaîne spécifiée contient des caractères null incorporés. |
| [**WindowsSubstring**](/windows/win32/api/winstring/nf-winstring-windowssubstring) | Récupère une sous-chaîne à partir de la chaîne spécifiée. La sous-chaîne commence à la position de caractère spécifiée. |
| [**WindowsSubstringWithSpecifiedLength**](/windows/win32/api/winstring/nf-winstring-windowssubstringwithspecifiedlength) | Récupère une sous-chaîne à partir de la chaîne spécifiée. La sous-chaîne commence à une position de caractère spécifiée et sa longueur est définie. |
| [**WindowsTrimStringEnd**](/windows/win32/api/winstring/nf-winstring-windowstrimstringend) | Supprime toutes les occurrences de fin d’un jeu de caractères spécifié de la chaîne source. |
| [**WindowsTrimStringStart**](/windows/win32/api/winstring/nf-winstring-windowstrimstringstart) | Supprime toutes les occurrences de début d’un jeu de caractères spécifié de la chaîne source. |



 

 

 
