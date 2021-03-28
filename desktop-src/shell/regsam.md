---
description: Type de données utilisé pour spécifier les attributs d’accès de sécurité dans le registre.
title: REGSAM (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983087"
---
# <a name="regsam"></a><span data-ttu-id="8aeb7-103">REGSAM</span><span class="sxs-lookup"><span data-stu-id="8aeb7-103">REGSAM</span></span>

<span data-ttu-id="8aeb7-104">Type de données utilisé pour spécifier les attributs d’accès de sécurité dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-104">A data type used for specifying the security access attributes in the registry.</span></span>



| <span data-ttu-id="8aeb7-105">Constante</span><span class="sxs-lookup"><span data-stu-id="8aeb7-105">Constant</span></span>                                                                                                                                                                                   | <span data-ttu-id="8aeb7-106">Description</span><span class="sxs-lookup"><span data-stu-id="8aeb7-106">Description</span></span>                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <span data-ttu-id="8aeb7-107"><dt>**\_tout \_ accéder à la clé**</dt></span><span class="sxs-lookup"><span data-stu-id="8aeb7-107"><dt>**KEY\_ALL\_ACCESS**</dt></span></span> </dl>                          | <span data-ttu-id="8aeb7-108">Combinaison de \* \* \* \* valeur de requête de clé \_ \_ \* \* \* \*, \* \* \* \* clé d' \_ énumération des \_ sous- \_ clés \* \* \_ \_ \_ \_ \_ \_ \_ \* \* \* \* \_ \* \* \* clé de notification \* \* \* \* \* \* \* \* \* clé de création de sous-clé \* \* \* \* \* \* \* \* \* \* clé de jeu de clés \* \* \* \* accès.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-108">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, \*\*\*\*KEY\_NOTIFY\*\*\*\*, \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\*, \*\*\*\*KEY\_CREATE\_LINK\*\*\*\*, and \*\*\*\*KEY\_SET\_VALUE\*\*\*\* access.</span></span><br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <span data-ttu-id="8aeb7-109"><dt>**\_lien de création de clé \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8aeb7-109"><dt>**KEY\_CREATE\_LINK**</dt></span></span> </dl>                       | <span data-ttu-id="8aeb7-110">Autorisation de créer un lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-110">Permission to create a symbolic link.</span></span><br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <span data-ttu-id="8aeb7-111"><dt>**CLÉ \_ créer une \_ sous- \_ clé**</dt></span><span class="sxs-lookup"><span data-stu-id="8aeb7-111"><dt>**KEY\_CREATE\_SUB\_KEY**</dt></span></span> </dl>             | <span data-ttu-id="8aeb7-112">Autorisation de créer des sous-clés.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-112">Permission to create subkeys.</span></span><br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <span data-ttu-id="8aeb7-113"><dt>**CLÉ \_ énumérer les \_ sous- \_ clés**</dt></span><span class="sxs-lookup"><span data-stu-id="8aeb7-113"><dt>**KEY\_ENUMERATE\_SUB\_KEYS**</dt></span></span> </dl> | <span data-ttu-id="8aeb7-114">Autorisation d’énumérer les sous-clés.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-114">Permission to enumerate subkeys.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <span data-ttu-id="8aeb7-115"><dt>**exécution de la clé \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8aeb7-115"><dt>**KEY\_EXECUTE**</dt></span></span> </dl>                                    | <span data-ttu-id="8aeb7-116">Autorisation pour l’accès en lecture.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-116">Permission for read access.</span></span><br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <span data-ttu-id="8aeb7-117"><dt>**CLÉ de \_ notification**</dt></span><span class="sxs-lookup"><span data-stu-id="8aeb7-117"><dt>**KEY\_NOTIFY**</dt></span></span> </dl>                                       | <span data-ttu-id="8aeb7-118">Autorisation pour la notification de modification.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-118">Permission for change notification.</span></span><br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <span data-ttu-id="8aeb7-119"><dt>**\_valeur de requête de clé \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8aeb7-119"><dt>**KEY\_QUERY\_VALUE**</dt></span></span> </dl>                       | <span data-ttu-id="8aeb7-120">Autorisation d’interroger les données de la sous-clé.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-120">Permission to query subkey data.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <span data-ttu-id="8aeb7-121"><dt>**lecture de la clé \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8aeb7-121"><dt>**KEY\_READ**</dt></span></span> </dl>                                             | <span data-ttu-id="8aeb7-122">Combinaison de \* \* \* \* valeur de requête de clé \_ \_ \* \* \* \*, \* \* \* \* clé \_ énumérer \_ les sous- \_ clés \* \* \* \* et \* \* \* \* clé de \_ notification \* \* \* \* \* accès.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-122">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, and \*\*\*\*KEY\_NOTIFY\*\*\*\* access.</span></span><br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <span data-ttu-id="8aeb7-123"><dt>**\_valeur du jeu de clés \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8aeb7-123"><dt>**KEY\_SET\_VALUE**</dt></span></span> </dl>                             | <span data-ttu-id="8aeb7-124">Autorisation de définir des données de sous-clé.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-124">Permission to set subkey data.</span></span><br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <span data-ttu-id="8aeb7-125"><dt>**écriture de clé \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8aeb7-125"><dt>**KEY\_WRITE**</dt></span></span> </dl>                                          | <span data-ttu-id="8aeb7-126">Combinaison de \* \* \* \* \_ valeur de jeu de clés \_ \* \* \* \* et \* \* \* \* clé \_ Create \_ Sub \_ Key \* \* \* \* Access.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-126">Combination of \*\*\*\*KEY\_SET\_VALUE\*\*\*\* and \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\* access.</span></span><br/>                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="8aeb7-127">Notes</span><span class="sxs-lookup"><span data-stu-id="8aeb7-127">Remarks</span></span>

<span data-ttu-id="8aeb7-128">Une valeur **REGSAM** peut être une ou plusieurs des valeurs listées.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-128">A **REGSAM** value can be one or more of the listed values.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aeb7-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8aeb7-129">Requirements</span></span>



| <span data-ttu-id="8aeb7-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8aeb7-130">Requirement</span></span> | <span data-ttu-id="8aeb7-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8aeb7-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8aeb7-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="8aeb7-132">Header</span></span><br/> | <dl> <span data-ttu-id="8aeb7-133"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aeb7-133"><dt>Winnt.h</dt></span></span> </dl> |



 

 




