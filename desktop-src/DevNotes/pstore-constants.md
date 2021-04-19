---
description: Les constantes suivantes sont utilisées par PStore.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: Constantes PStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 1c80fe7235a859ef0a754420fe5bd22caa10d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525480"
---
# <a name="pstore-constants"></a><span data-ttu-id="facdf-103">Constantes PStore</span><span class="sxs-lookup"><span data-stu-id="facdf-103">PStore Constants</span></span>

<span data-ttu-id="facdf-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="facdf-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="facdf-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="facdf-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="facdf-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="facdf-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="facdf-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="facdf-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="facdf-108">Les constantes suivantes sont utilisées par PStore.</span><span class="sxs-lookup"><span data-stu-id="facdf-108">The following constants are used by PStore.</span></span>

<span data-ttu-id="facdf-109">Codes d’erreur de stockage protégé</span><span class="sxs-lookup"><span data-stu-id="facdf-109">Protected Storage Error Codes</span></span>



| <span data-ttu-id="facdf-110">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="facdf-110">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="facdf-111">Description</span><span class="sxs-lookup"><span data-stu-id="facdf-111">Description</span></span>                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <span data-ttu-id="facdf-112"><dt>**Fichier PST \_ E \_ OK**</dt> <dt>0x00000000L</dt></span><span class="sxs-lookup"><span data-stu-id="facdf-112"><dt>**PST\_E\_OK**</dt> <dt>0x00000000L</dt></span></span> </dl>                             | <span data-ttu-id="facdf-113">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="facdf-113">The operation was successful.</span></span><br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <span data-ttu-id="facdf-114"><dt>**Fichier PST \_ Le \_ type E \_ existe**</dt> <dt>0x800C0004L</dt></span><span class="sxs-lookup"><span data-stu-id="facdf-114"><dt>**PST\_E\_TYPE\_EXISTS**</dt> <dt>0x800C0004L</dt></span></span> </dl> | <span data-ttu-id="facdf-115">L’élément de données existe déjà dans le stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="facdf-115">The data item already exists in the protected storage.</span></span> <br/> |



<span data-ttu-id="facdf-116">Valeurs de clause d’accès</span><span class="sxs-lookup"><span data-stu-id="facdf-116">Access Clause Values</span></span>



| <span data-ttu-id="facdf-117">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="facdf-117">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="facdf-118">Description</span><span class="sxs-lookup"><span data-stu-id="facdf-118">Description</span></span>                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <span data-ttu-id="facdf-119"><dt>**Fichier PST \_ AUTHENTICODE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="facdf-119"><dt>**PST\_AUTHENTICODE**</dt> <dt>1</dt></span></span> </dl>                       | <span data-ttu-id="facdf-120">Pointe vers une [**structure \_ AUTHENTICODEDATA PST**](pst-authenticodedata.md) .</span><span class="sxs-lookup"><span data-stu-id="facdf-120">Points to a [**PST\_AUTHENTICODEDATA**](pst-authenticodedata.md) structure.</span></span><br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <span data-ttu-id="facdf-121"><dt> **\_ \_ Vérification binaire PST**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="facdf-121"><dt>**PST\_BINARY\_CHECK** </dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="facdf-122">Pointe vers une **structure \_ BINARYCHECKDATA PST** .</span><span class="sxs-lookup"><span data-stu-id="facdf-122">Points to a **PST\_BINARYCHECKDATA** structure.</span></span><br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <span data-ttu-id="facdf-123"><dt>**Fichier PST \_ \_Descripteur de sécurité**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="facdf-123"><dt>**PST\_SECURITY\_DESCRIPTOR**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="facdf-124">Pointe vers un descripteur de sécurité Windows valide.</span><span class="sxs-lookup"><span data-stu-id="facdf-124">Points to a valid Windows security descriptor.</span></span> <br/>                              |



## <a name="requirements"></a><span data-ttu-id="facdf-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="facdf-125">Requirements</span></span>



| <span data-ttu-id="facdf-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="facdf-126">Requirement</span></span> | <span data-ttu-id="facdf-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="facdf-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="facdf-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="facdf-128">Header</span></span><br/> | <dl> <span data-ttu-id="facdf-129"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="facdf-129"><dt>Pstore.h</dt></span></span> </dl> |



 

 
