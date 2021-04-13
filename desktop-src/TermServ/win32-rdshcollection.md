---
title: Classe Win32_RDSHCollection
description: Gère une collection d’hôtes de session Bureau à distance.
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Win32_RDSHCollection de la classe Services Bureau à distance
- Win32_RDSHCollection de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465550"
---
# <a name="win32_rdshcollection-class"></a><span data-ttu-id="b8945-105">\_Classe RDSHCollection Win32</span><span class="sxs-lookup"><span data-stu-id="b8945-105">Win32\_RDSHCollection class</span></span>

<span data-ttu-id="b8945-106">Gère une collection d’hôtes de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b8945-106">Manages a collection of Remote Desktop Session Hosts.</span></span>

<span data-ttu-id="b8945-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b8945-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8945-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8945-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="b8945-109">Membres</span><span class="sxs-lookup"><span data-stu-id="b8945-109">Members</span></span>

<span data-ttu-id="b8945-110">La classe **Win32 \_ RDSHCollection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b8945-110">The **Win32\_RDSHCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="b8945-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b8945-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b8945-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b8945-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b8945-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b8945-113">Methods</span></span>

<span data-ttu-id="b8945-114">La classe **Win32 \_ RDSHCollection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b8945-114">The **Win32\_RDSHCollection** class has these methods.</span></span>



| <span data-ttu-id="b8945-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="b8945-115">Method</span></span>                                                                      | <span data-ttu-id="b8945-116">Description</span><span class="sxs-lookup"><span data-stu-id="b8945-116">Description</span></span>                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8945-117">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="b8945-117">**GetInt32Property**</span></span>](getint32property-win32-rdshcollection.md)           | <span data-ttu-id="b8945-118">Récupère une valeur de propriété entière d’un objet **Win32 \_ RDSHCollection** .</span><span class="sxs-lookup"><span data-stu-id="b8945-118">Retrieves an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="b8945-119">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="b8945-119">**GetStringProperty**</span></span>](getstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="b8945-120">Récupère une valeur de propriété de type chaîne d’un objet **Win32 \_ RDSHCollection** .</span><span class="sxs-lookup"><span data-stu-id="b8945-120">Retrieves a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="b8945-121">**KeyValueCompareAndSet**</span><span class="sxs-lookup"><span data-stu-id="b8945-121">**KeyValueCompareAndSet**</span></span>](win32-rdshcollection-keyvaluecompareandset.md) | <span data-ttu-id="b8945-122">Compare la clé spécifiée dans la collection avec un comparand ; Si elles correspondent, la nouvelle valeur est affectée à la clé.</span><span class="sxs-lookup"><span data-stu-id="b8945-122">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="b8945-123">Si la clé n’existe pas, la méthode insère la clé dans la collection.</span><span class="sxs-lookup"><span data-stu-id="b8945-123">If the key does not exist, the method will insert the key into the collection.</span></span><br/> |
| [<span data-ttu-id="b8945-124">**KeyValueDelete**</span><span class="sxs-lookup"><span data-stu-id="b8945-124">**KeyValueDelete**</span></span>](win32-rdshcollection-keyvaluedelete.md)               | <span data-ttu-id="b8945-125">Supprime la clé spécifiée (et la valeur associée) de la collection.</span><span class="sxs-lookup"><span data-stu-id="b8945-125">Deletes the specified key (and associated value) from the collection.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="b8945-126">**KeyValueGet**</span><span class="sxs-lookup"><span data-stu-id="b8945-126">**KeyValueGet**</span></span>](win32-rdshcollection-keyvalueget.md)                     | <span data-ttu-id="b8945-127">Récupère la valeur associée à la clé spécifiée dans la collection.</span><span class="sxs-lookup"><span data-stu-id="b8945-127">Retrieves the value associated with the specified key in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="b8945-128">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="b8945-128">**SetInt32Property**</span></span>](setint32property-win32-rdshcollection.md)           | <span data-ttu-id="b8945-129">Met à jour une valeur de propriété entière d’un objet **Win32 \_ RDSHCollection** .</span><span class="sxs-lookup"><span data-stu-id="b8945-129">Updates an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="b8945-130">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="b8945-130">**SetStringProperty**</span></span>](setstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="b8945-131">Met à jour une valeur de propriété de type chaîne d’un objet **Win32 \_ RDSHCollection** .</span><span class="sxs-lookup"><span data-stu-id="b8945-131">Updates a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="b8945-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b8945-132">Properties</span></span>

<span data-ttu-id="b8945-133">La classe **Win32 \_ RDSHCollection** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b8945-133">The **Win32\_RDSHCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8945-134">**Alias**</span><span class="sxs-lookup"><span data-stu-id="b8945-134">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8945-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8945-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8945-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b8945-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b8945-137">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b8945-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b8945-138">Obtient et définit l’alias de la collection.</span><span class="sxs-lookup"><span data-stu-id="b8945-138">Gets and sets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="b8945-139">**Description**</span><span class="sxs-lookup"><span data-stu-id="b8945-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8945-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8945-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8945-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b8945-141">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b8945-142">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b8945-142">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b8945-143">Obtient et définit la description de la collection.</span><span class="sxs-lookup"><span data-stu-id="b8945-143">Gets and sets the description of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="b8945-144">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b8945-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8945-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8945-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8945-146">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b8945-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8945-147">Obtient et définit le nom de la collection.</span><span class="sxs-lookup"><span data-stu-id="b8945-147">Gets and sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="b8945-148">**Type**</span><span class="sxs-lookup"><span data-stu-id="b8945-148">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8945-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8945-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8945-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b8945-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8945-151">**Windows server 2012 R2 et Windows server 2012 :** Cette propriété n’est pas disponible avant Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="b8945-151">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

<span data-ttu-id="b8945-152">Type de collection.</span><span class="sxs-lookup"><span data-stu-id="b8945-152">The type of collection.</span></span>

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="b8945-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Normal** (0)</span><span class="sxs-lookup"><span data-stu-id="b8945-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Regular** (0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b8945-154">(2)</span><span class="sxs-lookup"><span data-stu-id="b8945-154">(2)</span></span>


</dt> <dd>

<span data-ttu-id="b8945-155">Réservé</span><span class="sxs-lookup"><span data-stu-id="b8945-155">Reserved</span></span>

</dd> <dt>



 <span data-ttu-id="b8945-156">(3)</span><span class="sxs-lookup"><span data-stu-id="b8945-156">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b8945-157">Réservé</span><span class="sxs-lookup"><span data-stu-id="b8945-157">Reserved</span></span>

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span data-ttu-id="b8945-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)</span><span class="sxs-lookup"><span data-stu-id="b8945-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span data-ttu-id="b8945-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**Autopersonation** (5)</span><span class="sxs-lookup"><span data-stu-id="b8945-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**AutoPersonal** (5)</span></span>


<span data-ttu-id="b8945-160"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b8945-160"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b8945-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8945-161">Requirements</span></span>



| <span data-ttu-id="b8945-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8945-162">Requirement</span></span> | <span data-ttu-id="b8945-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8945-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8945-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8945-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b8945-165">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8945-165">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b8945-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8945-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b8945-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8945-167">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b8945-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b8945-168">Namespace</span></span><br/>                | <span data-ttu-id="b8945-169">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="b8945-169">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b8945-170">MOF</span><span class="sxs-lookup"><span data-stu-id="b8945-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8945-171"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8945-171"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8945-172">DLL</span><span class="sxs-lookup"><span data-stu-id="b8945-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8945-173"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8945-173"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b8945-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8945-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8945-175">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="b8945-175">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

