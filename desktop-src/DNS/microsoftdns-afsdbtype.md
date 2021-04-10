---
title: Classe MicrosoftDNS_AFSDBType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de serveur de base de données du système de fichiers Andrew (AFSDB).
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- MicrosoftDNS_AFSDBType de la classe DNS
- MicrosoftDNS_AFSDBType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
- MicrosoftDNS_AFSDBType.Modify
- MicrosoftDNS_AFSDBType.Subtype
- MicrosoftDNS_AFSDBType.ServerName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 836de50f4da9e613fb3e940b90971f38a634c804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032876"
---
# <a name="microsoftdns_afsdbtype-class"></a><span data-ttu-id="cff17-105">MicrosoftDNS \_ AFSDBType, classe</span><span class="sxs-lookup"><span data-stu-id="cff17-105">MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="cff17-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de serveur de base de données du système de fichiers Andrew (AFSDB).</span><span class="sxs-lookup"><span data-stu-id="cff17-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an Andrew File System Database Server (AFSDB) record.</span></span>

<span data-ttu-id="cff17-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="cff17-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cff17-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cff17-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a><span data-ttu-id="cff17-109">Membres</span><span class="sxs-lookup"><span data-stu-id="cff17-109">Members</span></span>

<span data-ttu-id="cff17-110">La classe **MicrosoftDNS \_ AFSDBType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cff17-110">The **MicrosoftDNS\_AFSDBType** class has these types of members:</span></span>

-   [<span data-ttu-id="cff17-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cff17-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="cff17-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cff17-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cff17-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cff17-113">Methods</span></span>

<span data-ttu-id="cff17-114">La classe **MicrosoftDNS \_ AFSDBType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cff17-114">The **MicrosoftDNS\_AFSDBType** class has these methods.</span></span>



| <span data-ttu-id="cff17-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="cff17-115">Method</span></span>                             | <span data-ttu-id="cff17-116">Description</span><span class="sxs-lookup"><span data-stu-id="cff17-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cff17-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="cff17-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="cff17-118">Instancie un enregistrement de ressource AFSDB en fonction des données des paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire/de la cellule, la classe (valeur par défaut = IN), la valeur de durée de vie et le sous-type et le nom du serveur AFS hôte.</span><span class="sxs-lookup"><span data-stu-id="cff17-118">Instantiates an AFSDB Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Cell Name, class (default = IN), time-to-live value, and host AFS server subtype and name.</span></span> <span data-ttu-id="cff17-119">Retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="cff17-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="cff17-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="cff17-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="cff17-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="cff17-121">**Modify**</span></span>                         | <span data-ttu-id="cff17-122">Cette méthode met à jour la durée de vie, le sous-type et le nom de serveur avec les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="cff17-122">This method updates the TTL, Subtype and Server Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="cff17-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="cff17-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="cff17-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="cff17-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="cff17-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="cff17-125">Qualifiers: Implemented</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="cff17-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cff17-126">Properties</span></span>

<span data-ttu-id="cff17-127">La classe **MicrosoftDNS \_ AFSDBType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cff17-127">The **MicrosoftDNS\_AFSDBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cff17-128">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="cff17-128">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cff17-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cff17-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cff17-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cff17-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cff17-131">Nom de domaine complet spécifiant un hôte qui a un serveur pour la cellule AFS spécifiée dans le nom du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="cff17-131">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="cff17-132">**Sous-type**</span><span class="sxs-lookup"><span data-stu-id="cff17-132">**Subtype**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cff17-133">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cff17-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cff17-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cff17-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cff17-135">Sous-type du serveur AFS hôte.</span><span class="sxs-lookup"><span data-stu-id="cff17-135">Subtype of the host AFS server.</span></span> <span data-ttu-id="cff17-136">Pour le sous-type 1 (valeur = 1), l’hôte dispose d’un serveur d’emplacement de volume AFS version 3,0 pour la cellule AFS nommée.</span><span class="sxs-lookup"><span data-stu-id="cff17-136">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="cff17-137">Dans le cas d’un sous-type 2 (valeur = 2), l’hôte dispose d’un serveur de noms authentifié contenant le nœud de répertoire racine de la cellule pour la cellule DCE/NCA nommée.</span><span class="sxs-lookup"><span data-stu-id="cff17-137">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cff17-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cff17-138">Requirements</span></span>



| <span data-ttu-id="cff17-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cff17-139">Requirement</span></span> | <span data-ttu-id="cff17-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="cff17-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cff17-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cff17-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cff17-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cff17-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cff17-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cff17-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cff17-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cff17-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cff17-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cff17-145">Namespace</span></span><br/>                | <span data-ttu-id="cff17-146">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="cff17-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cff17-147">MOF</span><span class="sxs-lookup"><span data-stu-id="cff17-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cff17-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cff17-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cff17-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cff17-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cff17-150">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="cff17-150">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="cff17-151">**Modifier la méthode de la \_ classe AFSDBType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cff17-151">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="cff17-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="cff17-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





