---
title: PeapServerUseAllPurposeCert
description: La clé de Registre PeapServerUseAllPurposeCert détermine si les certificats à usage général sont utilisés pour l’authentification PEAP.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104313834"
---
# <a name="peapserveruseallpurposecert"></a><span data-ttu-id="44072-103">PeapServerUseAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="44072-103">PeapServerUseAllPurposeCert</span></span>

<span data-ttu-id="44072-104">La clé de Registre PeapServerUseAllPurposeCert détermine si les certificats à usage général sont utilisés pour l’authentification PEAP.</span><span class="sxs-lookup"><span data-stu-id="44072-104">The PeapServerUseAllPurposeCert registry key determines if all-purpose certificates are used for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="44072-105">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="44072-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="44072-106">Notes</span><span class="sxs-lookup"><span data-stu-id="44072-106">Remarks</span></span>

<span data-ttu-id="44072-107">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="44072-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="44072-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="44072-108">Value</span></span>        | <span data-ttu-id="44072-109">Description</span><span class="sxs-lookup"><span data-stu-id="44072-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44072-110">1</span><span class="sxs-lookup"><span data-stu-id="44072-110">1</span></span>            | <span data-ttu-id="44072-111">Les certificats à usage général dans le magasin de certificats du client ou du serveur sont sélectionnés pour l’authentification PEAP.</span><span class="sxs-lookup"><span data-stu-id="44072-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="44072-112">Autres valeurs</span><span class="sxs-lookup"><span data-stu-id="44072-112">Other values</span></span> | <span data-ttu-id="44072-113">Les certificats à usage général dans le magasin de certificats du client ou du serveur ne sont pas sélectionnés pour l’authentification PEAP.</span><span class="sxs-lookup"><span data-stu-id="44072-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="44072-114">Si cette valeur de Registre n’est pas présente, les certificats à usage général dans le magasin de certificats du client ou du serveur sont sélectionnés pour l’authentification PEAP.</span><span class="sxs-lookup"><span data-stu-id="44072-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44072-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44072-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44072-116">Paramètres du Registre EAPHost</span><span class="sxs-lookup"><span data-stu-id="44072-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




