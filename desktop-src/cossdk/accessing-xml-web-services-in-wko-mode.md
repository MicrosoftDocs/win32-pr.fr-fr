---
description: vous pouvez accéder à un service web xml et l’utiliser, même si ce service web xml n’a pas été créé à l’aide de COM+ ou même de Microsoft Windows, à condition que le service web xml publie une description WSDL de sa syntaxe.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Accès aux services Web XML en mode WKO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013029"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a>Accès aux services Web XML en mode WKO

vous pouvez accéder à un service web xml et l’utiliser, même si ce service web xml n’a pas été créé à l’aide de COM+ ou même de Microsoft Windows, à condition que le service web xml publie une description WSDL de sa syntaxe. Il vous suffit de créer une instance du composant à l’aide du moniker SOAP : WSDL = URL, où URL est l’URL de la description WSDL du service Web XML auquel vous souhaitez accéder. Il s’agit du mode d’objet WKO (bien connu) qui consiste à accéder aux services Web XML.

Les méthodes de l’objet peuvent être appelées sans considérations particulières. Le service Web XML est accessible via une requête SOAP et la réponse est interprétée en toute transparence.

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Non applicable.

## <a name="visual-basic"></a>Visual Basic

le fragment de code Microsoft Visual Basic suivant illustre l’utilisation d’un service web XML en mode WKO.


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



Dans ce fragment de code qui illustre l’utilisation d’un composant d’une application COM+ exposée en tant que service Web XML, ServerName est le nom de domaine complet du serveur qui offre le service Web XML. vroot est le répertoire racine virtuel IIS à partir duquel le service Web XML est exposé. et progID est le ProgID du composant que vous souhaitez utiliser.

## <a name="cc"></a>C/C++

Le fragment de code suivant illustre l’utilisation d’un service Web XML en mode WKO.


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



Dans ce fragment de code qui illustre l’utilisation d’un composant d’une application COM+ exposée en tant que service Web XML, ServerName est le nom de domaine complet du serveur qui offre le service Web XML. vroot est le répertoire racine virtuel IIS à partir duquel le service Web XML est exposé. et progID est le ProgID du composant que vous souhaitez utiliser.

## <a name="remarks"></a>Notes

Lors du premier accès à un service Web XML en mode WKO, COM+ génère un client proxy et le compile en arrière-plan. Cette génération au moment de l’exécution et l’absence de connexions persistantes en mode WKO entraînent une réduction significative des performances par rapport au mode CAO.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès aux services Web XML en mode CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Vue d’ensemble du service SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Création de services Web XML](creating-xml-web-services.md)
</dt> <dt>

[Sécurisation des services Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 



