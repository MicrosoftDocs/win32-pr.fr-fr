---
description: Création d’objets BYOT
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Création d’objets BYOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544c5085061be5d1100706930a3e1617ec24890
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514529"
---
# <a name="creating-byot-objects"></a><span data-ttu-id="3ef0f-103">Création d’objets BYOT</span><span class="sxs-lookup"><span data-stu-id="3ef0f-103">Creating BYOT Objects</span></span>

<span data-ttu-id="3ef0f-104">Un nouvel objet BYOT crée des objets avec des transactions manuelles.</span><span class="sxs-lookup"><span data-stu-id="3ef0f-104">A new BYOT object creates objects with manual transactions.</span></span> <span data-ttu-id="3ef0f-105">Les deux interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) et [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), ont une méthode unique, **CreateInstance**, qui prend respectivement un pointeur d’interface **ITransaction** et une URL Tip.</span><span class="sxs-lookup"><span data-stu-id="3ef0f-105">The two interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) and [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), have a single method, **CreateInstance**, which take an **ITransaction** interface pointer and TIP URL, respectively.</span></span> <span data-ttu-id="3ef0f-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) retourne un pointeur d’interface vers l’objet nouvellement créé, qui est inscrit dans la transaction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3ef0f-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) returns an interface pointer to the newly created object, which is enlisted within the specified transaction.</span></span>

<span data-ttu-id="3ef0f-107">Lorsqu’un objet avec une transaction manuelle est publié, COM+ ne tente pas de valider la transaction.</span><span class="sxs-lookup"><span data-stu-id="3ef0f-107">When an object with a manual transaction is released, COM+ does not attempt to commit the transaction.</span></span> <span data-ttu-id="3ef0f-108">La transaction est contrôlée explicitement par le gestionnaire de transactions externe qui a distribué la transaction sous laquelle cet objet a été créé.</span><span class="sxs-lookup"><span data-stu-id="3ef0f-108">The transaction is controlled explicitly by the external transaction manager that dispensed the transaction under which this object had been created.</span></span>

> [!Note]  
> <span data-ttu-id="3ef0f-109">L’objet BYOT. ByotServerEx doit être importé dans une application COM+.</span><span class="sxs-lookup"><span data-stu-id="3ef0f-109">The Byot.ByotServerEx object needs to be imported into a COM+ application.</span></span>

 

 

 



