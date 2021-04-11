---
title: Modifier la méthode de la classe MicrosoftDNS_MGType
description: La méthode modify met à jour un enregistrement de ressource de groupe de messagerie (MG).
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_MGType classe
- MicrosoftDNS_MGType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706502569687a3c035c943e0a9dcc04aa1732492
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104737"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="c4046-106">Modifier la méthode de la \_ classe MGType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c4046-106">Modify method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="c4046-107">La méthode **Modify** met à jour un enregistrement de ressource de groupe de messagerie (mg).</span><span class="sxs-lookup"><span data-stu-id="c4046-107">The **Modify** method updates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4046-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4046-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c4046-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4046-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4046-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c4046-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4046-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="c4046-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c4046-112">*MGMailbox* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c4046-112">*MGMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4046-113">Nom de domaine complet spécifiant une boîte aux lettres qui est membre du groupe de messagerie spécifié par le nom du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c4046-113">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="c4046-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c4046-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c4046-115">Référence à l’objet modifié.</span><span class="sxs-lookup"><span data-stu-id="c4046-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4046-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4046-116">Return value</span></span>

<span data-ttu-id="c4046-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c4046-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4046-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c4046-118">Remarks</span></span>

<span data-ttu-id="c4046-119">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="c4046-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4046-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4046-120">Requirements</span></span>



| <span data-ttu-id="c4046-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4046-121">Requirement</span></span> | <span data-ttu-id="c4046-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4046-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4046-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4046-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c4046-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4046-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c4046-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4046-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c4046-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4046-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c4046-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c4046-127">Namespace</span></span><br/>                | <span data-ttu-id="c4046-128">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="c4046-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c4046-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c4046-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4046-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4046-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4046-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4046-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4046-132">**MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="c4046-132">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="c4046-133">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MGType**</span><span class="sxs-lookup"><span data-stu-id="c4046-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c4046-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c4046-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





