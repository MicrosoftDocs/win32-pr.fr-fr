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
# <a name="adsi-component-interaction"></a><span data-ttu-id="60cbc-103">Interaction des composants ADSI</span><span class="sxs-lookup"><span data-stu-id="60cbc-103">ADSI Component Interaction</span></span>

<span data-ttu-id="60cbc-104">Le composant routeur Active Directory remplit une table du fournisseur ADSI à partir des fournisseurs ADSI installés figurant dans le Registre lorsqu’il reçoit la première demande de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="60cbc-104">The Active Directory router component populates an ADSI provider table from the installed ADSI providers listed in the registry when it receives the first request from the client application.</span></span> <span data-ttu-id="60cbc-105">Pour plus d’informations sur le registre, consultez [installation du composant de l’exemple de fournisseur](installing-the-example-provider-component.md).</span><span class="sxs-lookup"><span data-stu-id="60cbc-105">For more information about the Registry, see [Installing the Example Provider Component](installing-the-example-provider-component.md).</span></span>

<span data-ttu-id="60cbc-106">Les opérations qui effectuent une requête à partir d’un répertoire pour un pointeur vers une interface sur un objet Active Directory proviennent d’une fonction (**GetObject** dans Visual Basic ou [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) en C ou C++), ou d’une méthode d’interface ( [**IADsContainer :: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)).</span><span class="sxs-lookup"><span data-stu-id="60cbc-106">Operations that make a request from a directory for a pointer to an interface on an Active Directory object come through a function (**GetObject** in Visual Basic or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C or C++), or an interface method ( [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)).</span></span> <span data-ttu-id="60cbc-107">Dans l’illustration suivante, l’application cliente ADSI passe une telle demande de liaison au composant de routeur ADSI (1).</span><span class="sxs-lookup"><span data-stu-id="60cbc-107">In the following figure, the ADSI client application passes such a bind request to the ADSI router component (1).</span></span> <span data-ttu-id="60cbc-108">Le composant routeur identifie le ProgID pour le fournisseur de la première partie de l’ADsPath et utilise [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) pour rechercher le CLSID correspondant dans le registre (2) et charge le composant fournisseur approprié (3).</span><span class="sxs-lookup"><span data-stu-id="60cbc-108">The router component identifies the ProgID for the provider from the first part of the ADsPath and uses [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) to find the matching CLSID in the registry (2) and loads the proper provider component (3).</span></span>

![interactions du composant ADSI dans l’exemple de fournisseur](images/dscspr.png)

<span data-ttu-id="60cbc-110">Dans l’illustration précédente, le composant fournisseur crée un objet Active Directory représentant l’élément répertoire nommé.</span><span class="sxs-lookup"><span data-stu-id="60cbc-110">In the preceding figure, the provider component creates an Active Directory object representing the named directory element.</span></span> <span data-ttu-id="60cbc-111">Le composant de prise en charge ADSI effectue une **QueryInterface** sur l’identificateur d’interface demandé.</span><span class="sxs-lookup"><span data-stu-id="60cbc-111">The ADSI support component does a **QueryInterface** on the requested interface identifier.</span></span> <span data-ttu-id="60cbc-112">Quand un pointeur vers cette interface est récupéré (4), comme avec toutes les implémentations de client/serveur COM, il est ensuite renvoyé au client (5), puis à partir de l’application cliente directement avec le composant fournisseur (6).</span><span class="sxs-lookup"><span data-stu-id="60cbc-112">When a pointer to that interface is retrieved (4), as with all COM client/server implementations, it is then passed back to the client (5), and from then on the client application works directly with the provider component (6).</span></span>

 

 