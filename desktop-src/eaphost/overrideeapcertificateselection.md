---
title: OverrideEAPCertificateSelection
description: La clé de Registre OverrideEAPCertificateSelection détermine si le client remplacera le comportement de sélection de certificat de carte à puce par défaut et fournira à l’utilisateur plus de certificats à choisir.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d958eeeffba96e7a060ee4dd3edaf8a9935a15d1
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103841741"
---
# <a name="overrideeapcertificateselection"></a><span data-ttu-id="2b1b8-103">OverrideEAPCertificateSelection</span><span class="sxs-lookup"><span data-stu-id="2b1b8-103">OverrideEAPCertificateSelection</span></span>

<span data-ttu-id="2b1b8-104">La clé de Registre OverrideEAPCertificateSelection détermine si le client remplacera le comportement de sélection de certificat de carte à puce par défaut et fournira à l’utilisateur plus de certificats à choisir.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-104">The OverrideEAPCertificateSelection registry key determines whether the client will override the default smart card certificate selection behavior and provide the user with more certificates to choose from.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="2b1b8-105">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="2b1b8-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a><span data-ttu-id="2b1b8-106">Notes</span><span class="sxs-lookup"><span data-stu-id="2b1b8-106">Remarks</span></span>

<span data-ttu-id="2b1b8-107">Il s’agit d’une valeur **\_ binaire de Reg** .</span><span class="sxs-lookup"><span data-stu-id="2b1b8-107">This is a **REG\_BINARY** value.</span></span>



| <span data-ttu-id="2b1b8-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b1b8-108">Value</span></span> | <span data-ttu-id="2b1b8-109">Description</span><span class="sxs-lookup"><span data-stu-id="2b1b8-109">Description</span></span>                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1b8-110">0x000</span><span class="sxs-lookup"><span data-stu-id="2b1b8-110">0x000</span></span> | <span data-ttu-id="2b1b8-111">Ne substituez pas le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-111">Do not override the default behavior.</span></span>                                                                                                                                                                |
| <span data-ttu-id="2b1b8-112">0x001</span><span class="sxs-lookup"><span data-stu-id="2b1b8-112">0x001</span></span> | <span data-ttu-id="2b1b8-113">Choisissez le dernier certificat attaché à partir de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-113">Choose the last attached certificate from the smart card.</span></span>                                                                                                                                            |
| <span data-ttu-id="2b1b8-114">0x010</span><span class="sxs-lookup"><span data-stu-id="2b1b8-114">0x010</span></span> | <span data-ttu-id="2b1b8-115">Affiche tous les certificats dans l’interface utilisateur de sélection de certificat à partir de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-115">Shows all certificates in the certificate selection UI from the smart card.</span></span>                                                                                                                          |
| <span data-ttu-id="2b1b8-116">0x100</span><span class="sxs-lookup"><span data-stu-id="2b1b8-116">0x100</span></span> | <span data-ttu-id="2b1b8-117">Affiche tous les certificats de l’interface utilisateur de sélection de certificat à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-117">Shows all certificates in the certificate selection UI from the registry.</span></span>                                                                                                                            |
| <span data-ttu-id="2b1b8-118">0x101</span><span class="sxs-lookup"><span data-stu-id="2b1b8-118">0x101</span></span> | <span data-ttu-id="2b1b8-119">Affiche tous les certificats de l’interface utilisateur de sélection de certificat à partir du Registre et le dernier certificat attaché à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-119">Shows all certificates in the certificate selection UI from the registry and the last attached certificate from the smart card.</span></span> <span data-ttu-id="2b1b8-120">Affiche le dernier certificat attaché à partir de la carte à puce comme sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-120">Shows the last attached certificate from the smart card as selected.</span></span> |
| <span data-ttu-id="2b1b8-121">0x110</span><span class="sxs-lookup"><span data-stu-id="2b1b8-121">0x110</span></span> | <span data-ttu-id="2b1b8-122">Affiche tous les certificats de l’interface utilisateur de sélection de certificat à partir du Registre et de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-122">Shows all certificates in the certificate selection UI from the registry and the smart card.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="2b1b8-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b1b8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b1b8-124">Paramètres du Registre EAPHost</span><span class="sxs-lookup"><span data-stu-id="2b1b8-124">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




