---
title: Déplacement d’objets
description: Déplacement d’objets
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Exemples de Active Directory Active Directory, déplacement d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030997"
---
# <a name="moving-objects"></a><span data-ttu-id="20400-104">Déplacement d’objets</span><span class="sxs-lookup"><span data-stu-id="20400-104">Moving Objects</span></span>

<span data-ttu-id="20400-105">Pour déplacer un objet au sein d’un domaine, utilisez la méthode [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .</span><span class="sxs-lookup"><span data-stu-id="20400-105">To move an object within a domain, use the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="20400-106">**Pour déplacer un objet dans un domaine**</span><span class="sxs-lookup"><span data-stu-id="20400-106">**To move an object within a domain**</span></span>

1.  <span data-ttu-id="20400-107">Crée une liaison avec l’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) de l’objet à déplacer.</span><span class="sxs-lookup"><span data-stu-id="20400-107">Bind to the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface of the object to move.</span></span>
2.  <span data-ttu-id="20400-108">Obtient l’ADsPath de l’objet à déplacer à partir de la propriété [**IADs. ADsPath**](/windows/desktop/ADSI/iads-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="20400-108">Get the ADsPath of the object to move from the [**IADs.ADsPath**](/windows/desktop/ADSI/iads-property-methods) property.</span></span>
3.  <span data-ttu-id="20400-109">Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) du conteneur dans lequel l’objet sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="20400-109">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface of the container where the object will be moved to.</span></span>
4.  <span data-ttu-id="20400-110">Déplacez l’objet avec la méthode [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .</span><span class="sxs-lookup"><span data-stu-id="20400-110">Move the object with the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="20400-111">S’il existe une interface pour l’objet qui a été déplacé, l’interface n’est pas valide après le déplacement de l’objet, car l’objet d’annuaire représenté par l’interface n’existe plus.</span><span class="sxs-lookup"><span data-stu-id="20400-111">If an interface exists to the object that was moved, the interface is not valid after the object is moved because the directory object the interface represents no longer exists.</span></span>

<span data-ttu-id="20400-112">Pour plus d’informations et pour obtenir un exemple de code qui montre comment déplacer un objet, consultez l' [exemple de code pour déplacer un objet](example-code-for-moving-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="20400-112">For more information and a code example that shows how to move an object, see [Example Code for Moving an Object](example-code-for-moving-an-object.md).</span></span>

 

 