---
title: Désinscription IAgent
description: Désinscription IAgent
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842281"
---
# <a name="iagentunregister"></a><span data-ttu-id="cf424-103">IAgent :: Unregister</span><span class="sxs-lookup"><span data-stu-id="cf424-103">IAgent::Unregister</span></span>

<span data-ttu-id="cf424-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cf424-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

<span data-ttu-id="cf424-105">Décharge les données caractères pour le caractère spécifié à partir de la collection de [**caractères**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="cf424-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="cf424-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="cf424-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cf424-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*</span><span class="sxs-lookup"><span data-stu-id="cf424-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="cf424-108">ID du récepteur de notifications.</span><span class="sxs-lookup"><span data-stu-id="cf424-108">The notification sink ID.</span></span>

</dd> </dl>

<span data-ttu-id="cf424-109">Utilisez cette méthode lorsque vous n’avez plus besoin des services Microsoft Agent, tels que le moment où votre application s’arrête.</span><span class="sxs-lookup"><span data-stu-id="cf424-109">Use this method when you no longer need Microsoft Agent services, such as when your application shuts down.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf424-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf424-110">See Also</span></span>

[<span data-ttu-id="cf424-111">**IAgent :: Register**</span><span class="sxs-lookup"><span data-stu-id="cf424-111">**IAgent::Register**</span></span>](iagent--register.md)


 

 