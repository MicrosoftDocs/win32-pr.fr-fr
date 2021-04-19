---
title: Modifier la méthode de la classe MicrosoftDNS_AFSDBType
description: La méthode modify met à jour un enregistrement de ressource de serveur de base de données (AFSDB) Andrew File System.
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_AFSDBType classe
- MicrosoftDNS_AFSDBType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4752910ab9e8117bfdaf27f93d32be3377158ba5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513603"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="49196-106">Modifier la méthode de la \_ classe AFSDBType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="49196-106">Modify method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="49196-107">La méthode **Modify** met à jour un enregistrement de ressource de serveur de base de données (AFSDB) Andrew File System.</span><span class="sxs-lookup"><span data-stu-id="49196-107">The **Modify** method updates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="49196-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49196-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="49196-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49196-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49196-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49196-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49196-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="49196-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="49196-112">*Sous-type* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49196-112">*Subtype* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49196-113">Sous-type du serveur AFS hôte.</span><span class="sxs-lookup"><span data-stu-id="49196-113">Subtype of the host AFS server.</span></span> <span data-ttu-id="49196-114">Pour le sous-type 1 (valeur = 1), l’hôte dispose d’un serveur d’emplacement de volume AFS version 3,0 pour la cellule AFS nommée.</span><span class="sxs-lookup"><span data-stu-id="49196-114">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="49196-115">Dans le cas d’un sous-type 2 (valeur = 2), l’hôte dispose d’un serveur de noms authentifié contenant le nœud de répertoire racine de la cellule pour la cellule DCE/NCA nommée.</span><span class="sxs-lookup"><span data-stu-id="49196-115">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="49196-116">*Nom du serveur* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49196-116">*ServerName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49196-117">Nom de domaine complet spécifiant un hôte qui a un serveur pour la cellule AFS spécifiée dans le nom du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="49196-117">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="49196-118">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="49196-118">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="49196-119">Référence à l’objet modifié.</span><span class="sxs-lookup"><span data-stu-id="49196-119">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49196-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49196-120">Return value</span></span>

<span data-ttu-id="49196-121">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="49196-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49196-122">Notes</span><span class="sxs-lookup"><span data-stu-id="49196-122">Remarks</span></span>

<span data-ttu-id="49196-123">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="49196-123">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="49196-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49196-124">Requirements</span></span>



| <span data-ttu-id="49196-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49196-125">Requirement</span></span> | <span data-ttu-id="49196-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="49196-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49196-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49196-127">Minimum supported client</span></span><br/> | <span data-ttu-id="49196-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="49196-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="49196-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49196-129">Minimum supported server</span></span><br/> | <span data-ttu-id="49196-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49196-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="49196-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="49196-131">Namespace</span></span><br/>                | <span data-ttu-id="49196-132">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="49196-132">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="49196-133">MOF</span><span class="sxs-lookup"><span data-stu-id="49196-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49196-134"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49196-134"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49196-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49196-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49196-136">**MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="49196-136">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="49196-137">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="49196-137">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="49196-138">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="49196-138">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





