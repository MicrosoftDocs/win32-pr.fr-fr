---
title: Classe MDM_Personalization
description: La \_ classe de personnalisation MDM est utilisée pour définir l’écran de verrouillage et les images d’arrière-plan du bureau. La définition de ces stratégies empêche également l’utilisateur de modifier l’image.
ms.assetid: 99b60767-b321-4ec6-9802-76221d26c830
keywords:
- Classe MDM_Personalization
- Classe MDM_Personalization, Description
topic_type:
- apiref
api_name:
- MDM_Personalization
- MDM_Personalization.InstanceID
- MDM_Personalization.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78986422cce15d750e1ae678aef352bbb369bfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941933"
---
# <a name="mdm_personalization-class"></a><span data-ttu-id="be87b-106">\_Classe de personnalisation MDM</span><span class="sxs-lookup"><span data-stu-id="be87b-106">MDM\_Personalization class</span></span>

<span data-ttu-id="be87b-107">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="be87b-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="be87b-108">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="be87b-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="be87b-109">La \_ classe de personnalisation MDM est utilisée pour définir l’écran de verrouillage et les images d’arrière-plan du bureau.</span><span class="sxs-lookup"><span data-stu-id="be87b-109">The MDM\_Personalization class is used to set the lock screen and desktop background images.</span></span> <span data-ttu-id="be87b-110">La définition de ces stratégies empêche également l’utilisateur de modifier l’image.</span><span class="sxs-lookup"><span data-stu-id="be87b-110">Setting these policies also prevents the user from changing the image.</span></span>

<span data-ttu-id="be87b-111">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="be87b-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="be87b-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be87b-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Personalization
{
  string InstanceID;
  string ParentID;
  string DesktopImageUrl;
  sint32 DesktopImageStatus;
  string LockScreenImageUrl;
  sint32 LockScreenImageStatus;
};
```

## <a name="members"></a><span data-ttu-id="be87b-113">Membres</span><span class="sxs-lookup"><span data-stu-id="be87b-113">Members</span></span>

<span data-ttu-id="be87b-114">La classe de **\_ personnalisation MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="be87b-114">The **MDM\_Personalization** class has these types of members:</span></span>

-   [<span data-ttu-id="be87b-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be87b-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be87b-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be87b-116">Properties</span></span>

<span data-ttu-id="be87b-117">La classe de **\_ personnalisation MDM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="be87b-117">The **MDM\_Personalization** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="be87b-118">DesktopImageStatus</span><span class="sxs-lookup"><span data-stu-id="be87b-118">DesktopImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#desktopimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be87b-119">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="be87b-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="be87b-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="be87b-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be87b-121">DesktopImageUrl</span><span class="sxs-lookup"><span data-stu-id="be87b-121">DesktopImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#desktopimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be87b-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be87b-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be87b-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="be87b-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be87b-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="be87b-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be87b-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be87b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be87b-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be87b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be87b-127">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="be87b-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be87b-128">LockScreenImageStatus</span><span class="sxs-lookup"><span data-stu-id="be87b-128">LockScreenImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be87b-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="be87b-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="be87b-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="be87b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be87b-131">LockScreenImageUrl</span><span class="sxs-lookup"><span data-stu-id="be87b-131">LockScreenImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be87b-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be87b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be87b-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="be87b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be87b-134">**ID**</span><span class="sxs-lookup"><span data-stu-id="be87b-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be87b-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be87b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be87b-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be87b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be87b-137">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="be87b-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be87b-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be87b-138">Requirements</span></span>



| <span data-ttu-id="be87b-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be87b-139">Requirement</span></span> | <span data-ttu-id="be87b-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="be87b-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be87b-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be87b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="be87b-142">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be87b-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be87b-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be87b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="be87b-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="be87b-144">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="be87b-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="be87b-145">Namespace</span></span><br/>                | <span data-ttu-id="be87b-146">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="be87b-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="be87b-147">MOF</span><span class="sxs-lookup"><span data-stu-id="be87b-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be87b-148"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be87b-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="be87b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="be87b-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be87b-150"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be87b-150"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

