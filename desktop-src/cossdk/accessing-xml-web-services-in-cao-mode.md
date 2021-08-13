---
description: Si le service Web XML auquel vous souhaitez accéder a été créé en exposant une application COM+, pensez à y accéder en mode de l’objet activé par le client (CAO), ce qui permet d’éviter la génération d’un proxy au moment de l’exécution et d’améliorer les performances à l’aide de connexions persistantes.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Accès aux services Web XML en mode CAO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e3f8dc1fa3c037d03d8b69cf45737c7211d92f7d38e733a97b9be109a2243a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549457"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a>Accès aux services Web XML en mode CAO

Si le service Web XML auquel vous souhaitez accéder a été créé en exposant une application COM+, pensez à y accéder en mode de l’objet activé par le client (CAO), ce qui permet d’éviter la génération d’un proxy au moment de l’exécution et d’améliorer les performances à l’aide de connexions persistantes. Pour accéder à un service Web XML en mode CAO, commencez par [Exporter](exporting-a-soap-enabled-application.md) l’application compatible SOAP correspondante à partir de votre serveur en mode proxy, puis [importez](importing-a-soap-enabled-application.md) l’application dans le client à partir duquel vous souhaitez accéder à l’application en tant que service Web XML. Les composants de l’application peuvent ensuite être instanciés sur le client comme les composants des applications locales, par exemple en utilisant **GetObject** et [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="user-interface"></a>Interface utilisateur

Non applicable.

## <a name="visual-basic"></a>Visual Basic

l’Visual Basic fragment de code suivant illustre l’utilisation d’un composant d’une application COM+ exposée en tant que service web XML en mode CAO.


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a>C/C++

Le fragment de code suivant illustre l’utilisation d’un composant d’une application COM+ exposée en tant que service Web XML en mode CAO.


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès aux services Web XML en mode WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Vue d’ensemble du service SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Création de services Web XML](creating-xml-web-services.md)
</dt> <dt>

[Sécurisation des services Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 
