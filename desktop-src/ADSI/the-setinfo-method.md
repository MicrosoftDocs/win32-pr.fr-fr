---
title: Méthode SetInfo
description: La méthode IADs SetInfo enregistre les valeurs actuelles des propriétés de cet objet Active Directory depuis le cache des propriétés vers le magasin d’annuaires sous-jacent. Cela est similaire au vidage d’une mémoire tampon sur le disque.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- SetInfo ADSI, utilisation
- propriétés ADSI, enregistrer les valeurs actuelles des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5965a46e5accd2a00adc006fe37511de13ff0df3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309214"
---
# <a name="the-setinfo-method"></a><span data-ttu-id="7650a-106">Méthode SetInfo</span><span class="sxs-lookup"><span data-stu-id="7650a-106">The SetInfo Method</span></span>

<span data-ttu-id="7650a-107">La méthode [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) enregistre les valeurs actuelles des propriétés de cet objet Active Directory depuis le cache des propriétés vers le magasin d’annuaires sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="7650a-107">The [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method saves the current values for the properties for this Active Directory object from the property cache to the underlying directory store.</span></span> <span data-ttu-id="7650a-108">Cela est similaire au vidage d’une mémoire tampon sur le disque.</span><span class="sxs-lookup"><span data-stu-id="7650a-108">This is analogous to flushing a buffer out to disk.</span></span>

<span data-ttu-id="7650a-109">[**Setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) met à jour les objets qui existent déjà dans l’annuaire, ou crée une entrée d’annuaire pour les objets nouvellement créés.</span><span class="sxs-lookup"><span data-stu-id="7650a-109">[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) updates objects that already exist in the directory, or create a new directory entry for newly created objects.</span></span>

<span data-ttu-id="7650a-110">Au moment de l’appel de [**setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , si des valeurs de cache de propriété ont été écrites [**avec un code de contrôle**](/windows/desktop/api/Iads/nf-iads-iads-putex) de point de contrôle d’état de la propriété, par exemple, \_ \_ la propriété ad Update ou ADS est \_ \_ désactivée, les demandes appropriées sont transmises au service d’annuaire sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="7650a-110">At the time of the [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) call, if any property cache values have been written with a [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) control code, such as ADS\_PROPERTY\_UPDATE or ADS\_PROPERTY\_CLEAR, then the appropriate requests are passed on to the underlying directory service.</span></span>

 

 




