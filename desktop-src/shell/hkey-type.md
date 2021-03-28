---
description: Ces types de données peuvent être utilisés pour spécifier le type d’une valeur de registre.
title: Types de données de Registre (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996592"
---
# <a name="registry-data-types"></a><span data-ttu-id="71562-103">Types de données de Registre</span><span class="sxs-lookup"><span data-stu-id="71562-103">Registry Data Types</span></span>

<span data-ttu-id="71562-104">Ces types de données peuvent être utilisés pour spécifier le type d’une valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="71562-104">These data types can be used to specify the type of a registry value.</span></span>



| <span data-ttu-id="71562-105">Constante</span><span class="sxs-lookup"><span data-stu-id="71562-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="71562-106">Description</span><span class="sxs-lookup"><span data-stu-id="71562-106">Description</span></span>                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <span data-ttu-id="71562-107"><dt>**\_fichier binaire reg**</dt></span><span class="sxs-lookup"><span data-stu-id="71562-107"><dt>**REG\_BINARY**</dt></span></span> </dl>                                          | <span data-ttu-id="71562-108">Données binaires dans tout formulaire.</span><span class="sxs-lookup"><span data-stu-id="71562-108">Binary data in any form.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <span data-ttu-id="71562-109"><dt>**\_valeur DWORD reg**</dt></span><span class="sxs-lookup"><span data-stu-id="71562-109"><dt>**REG\_DWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="71562-110">32-nombre de bits.</span><span class="sxs-lookup"><span data-stu-id="71562-110">32-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <span data-ttu-id="71562-111"><dt>**\_q QWord**</dt></span><span class="sxs-lookup"><span data-stu-id="71562-111"><dt>**REG\_QWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="71562-112">64-nombre de bits.</span><span class="sxs-lookup"><span data-stu-id="71562-112">64-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <span data-ttu-id="71562-113"><dt>**REG \_ DWORD \_ Little \_ ENDIAN**</dt></span><span class="sxs-lookup"><span data-stu-id="71562-113"><dt>**REG\_DWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="71562-114">32 bits au format avec primauté des octets de poids faible (Little endian).</span><span class="sxs-lookup"><span data-stu-id="71562-114">32-bit number in little-endian format.</span></span> <span data-ttu-id="71562-115">Cela équivaut à **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="71562-115">This is equivalent to **REG\_DWORD**.</span></span><br/> <span data-ttu-id="71562-116">Au format Little endian, une valeur multioctet est stockée en mémoire à partir de l’octet le plus bas (le « petit end ») jusqu’à l’octet le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="71562-116">In little-endian format, a multibyte value is stored in memory from the lowest byte (the "little end") to the highest byte.</span></span> <span data-ttu-id="71562-117">Par exemple, la valeur 0x12345678 sinon est stockée sous la forme (0x78 0x56 0x34 0x12) au format avec primauté des octets de poids faible (Little endian).</span><span class="sxs-lookup"><span data-stu-id="71562-117">For example, the value 0x12345678 is stored as (0x78 0x56 0x34 0x12) in little-endian format.</span></span><br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <span data-ttu-id="71562-118"><dt>**\_ \_ faible primauté des \_ octets de poids faible**</dt></span><span class="sxs-lookup"><span data-stu-id="71562-118"><dt>**REG\_QWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="71562-119">Nombre 64 bits au format avec primauté des octets de poids faible (Little endian).</span><span class="sxs-lookup"><span data-stu-id="71562-119">A 64-bit number in little-endian format.</span></span> <span data-ttu-id="71562-120">Cela équivaut à **reg \_ QWord**.</span><span class="sxs-lookup"><span data-stu-id="71562-120">This is equivalent to **REG\_QWORD**.</span></span> <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <span data-ttu-id="71562-121"><dt>**REG \_ DWORD \_ Big \_ ENDIAN**</dt></span><span class="sxs-lookup"><span data-stu-id="71562-121"><dt>**REG\_DWORD\_BIG\_ENDIAN**</dt></span></span> </dl>          | <span data-ttu-id="71562-122">32-nombre de bits au format Big-endian.</span><span class="sxs-lookup"><span data-stu-id="71562-122">32-bit number in big-endian format.</span></span><br/> <span data-ttu-id="71562-123">Au format Big-endian, une valeur multioctet est stockée en mémoire à partir de l’octet le plus élevé (le « Big end ») jusqu’à l’octet le plus bas.</span><span class="sxs-lookup"><span data-stu-id="71562-123">In big-endian format, a multibyte value is stored in memory from the highest byte (the "big end") to the lowest byte.</span></span> <span data-ttu-id="71562-124">Par exemple, la valeur 0x12345678 sinon est stockée sous la forme (0x12 0x34 0x56 0x78) au format Big-endian.</span><span class="sxs-lookup"><span data-stu-id="71562-124">For example, the value 0x12345678 is stored as (0x12 0x34 0x56 0x78) in big-endian format.</span></span><br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <span data-ttu-id="71562-125"><dt>**REG \_ développer \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="71562-125"><dt>**REG\_EXPAND\_SZ**</dt></span></span> </dl>                                | <span data-ttu-id="71562-126">Chaîne terminée par le caractère null qui contient des références non développées à des variables d’environnement (par exemple, "% PATH%").</span><span class="sxs-lookup"><span data-stu-id="71562-126">Null-terminated string that contains unexpanded references to environment variables (for example, "%PATH%").</span></span> <span data-ttu-id="71562-127">Il s’agit d’une chaîne Unicode ou ANSI, selon que vous utilisez les fonctions Unicode ou ANSI.</span><span class="sxs-lookup"><span data-stu-id="71562-127">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <span data-ttu-id="71562-128"><dt>**\_lien reg**</dt></span><span class="sxs-lookup"><span data-stu-id="71562-128"><dt>**REG\_LINK**</dt></span></span> </dl>                                                | <span data-ttu-id="71562-129">Lien symbolique Unicode.</span><span class="sxs-lookup"><span data-stu-id="71562-129">Unicode symbolic link.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <span data-ttu-id="71562-130"><dt>**REG \_ multiple \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="71562-130"><dt>**REG\_MULTI\_SZ**</dt></span></span> </dl>                                   | <span data-ttu-id="71562-131">Tableau de chaînes terminées par le caractère null qui se terminent par deux caractères null.</span><span class="sxs-lookup"><span data-stu-id="71562-131">Array of null-terminated strings that are terminated by two null characters.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <span data-ttu-id="71562-132"><dt>**REG \_ aucun**</dt></span><span class="sxs-lookup"><span data-stu-id="71562-132"><dt>**REG\_NONE**</dt></span></span> </dl>                                                | <span data-ttu-id="71562-133">Aucun type valeur défini.</span><span class="sxs-lookup"><span data-stu-id="71562-133">No defined value type.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <span data-ttu-id="71562-134"><dt>**\_liste des ressources reg \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71562-134"><dt>**REG\_RESOURCE\_LIST**</dt></span></span> </dl>                    | <span data-ttu-id="71562-135">Liste des ressources de pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="71562-135">Device-driver resource list.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <span data-ttu-id="71562-136"><dt>**SZ de REG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71562-136"><dt>**REG\_SZ**</dt></span></span> </dl>                                                      | <span data-ttu-id="71562-137">Chaîne terminée par un caractère Null.</span><span class="sxs-lookup"><span data-stu-id="71562-137">Null-terminated string.</span></span> <span data-ttu-id="71562-138">Il s’agit d’une chaîne Unicode ou ANSI, selon que vous utilisez les fonctions Unicode ou ANSI.</span><span class="sxs-lookup"><span data-stu-id="71562-138">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="71562-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="71562-139">Requirements</span></span>



| <span data-ttu-id="71562-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71562-140">Requirement</span></span> | <span data-ttu-id="71562-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="71562-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71562-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="71562-142">Header</span></span><br/> | <dl> <span data-ttu-id="71562-143"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="71562-143"><dt>Winnt.h</dt></span></span> </dl> |



 

 




