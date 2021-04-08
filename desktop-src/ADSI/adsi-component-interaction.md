---
title: Interaction des composants ADSI
description: Le composant routeur Active Directory remplit une table du fournisseur ADSI à partir des fournisseurs ADSI installés figurant dans le Registre lorsqu’il reçoit la première demande de l’application cliente.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a9ca749e1083ab86335893bef9f4307faee410
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730205"
---
# <a name="adsi-component-interaction"></a>Interaction des composants ADSI

Le composant routeur Active Directory remplit une table du fournisseur ADSI à partir des fournisseurs ADSI installés figurant dans le Registre lorsqu’il reçoit la première demande de l’application cliente. Pour plus d’informations sur le registre, consultez [installation du composant de l’exemple de fournisseur](installing-the-example-provider-component.md).

Les opérations qui effectuent une requête à partir d’un répertoire pour un pointeur vers une interface sur un objet Active Directory proviennent d’une fonction (**GetObject** dans Visual Basic ou [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) en C ou C++), ou d’une méthode d’interface ( [**IADsContainer :: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)). Dans l’illustration suivante, l’application cliente ADSI passe une telle demande de liaison au composant de routeur ADSI (1). Le composant routeur identifie le ProgID pour le fournisseur de la première partie de l’ADsPath et utilise [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) pour rechercher le CLSID correspondant dans le registre (2) et charge le composant fournisseur approprié (3).

![interactions du composant ADSI dans l’exemple de fournisseur](images/dscspr.png)

Dans l’illustration précédente, le composant fournisseur crée un objet Active Directory représentant l’élément répertoire nommé. Le composant de prise en charge ADSI effectue une **QueryInterface** sur l’identificateur d’interface demandé. Quand un pointeur vers cette interface est récupéré (4), comme avec toutes les implémentations de client/serveur COM, il est ensuite renvoyé au client (5), puis à partir de l’application cliente directement avec le composant fournisseur (6).

 

 