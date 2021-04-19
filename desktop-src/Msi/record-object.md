---
description: L’objet record est un conteneur destiné à contenir et à transférer un nombre variable de valeurs.
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Objet record
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c13cb31d628525e529491af1c089555ba2ad8273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521616"
---
# <a name="record-object"></a><span data-ttu-id="64056-103">Objet record</span><span class="sxs-lookup"><span data-stu-id="64056-103">Record object</span></span>

<span data-ttu-id="64056-104">L’objet **Record** est un conteneur destiné à contenir et à transférer un nombre variable de valeurs.</span><span class="sxs-lookup"><span data-stu-id="64056-104">The **Record** object is a container for holding and transferring a variable number of values.</span></span> <span data-ttu-id="64056-105">Les champs de l’enregistrement sont indexés numériquement et peuvent contenir des chaînes, des entiers, des objets et des valeurs NULL.</span><span class="sxs-lookup"><span data-stu-id="64056-105">Fields within the record are numerically indexed and can contain strings, integers, objects, and null values.</span></span> <span data-ttu-id="64056-106">Les champs au-delà de la taille des enregistrements alloués sont traités comme ayant des valeurs null de manière permanente.</span><span class="sxs-lookup"><span data-stu-id="64056-106">Fields beyond the allocated record size are treated as having permanently null values.</span></span> <span data-ttu-id="64056-107">Le champ numéro 0 est réservé.</span><span class="sxs-lookup"><span data-stu-id="64056-107">Field number 0 is reserved.</span></span>

## <a name="members"></a><span data-ttu-id="64056-108">Membres</span><span class="sxs-lookup"><span data-stu-id="64056-108">Members</span></span>

<span data-ttu-id="64056-109">L’objet **Record** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="64056-109">The **Record** object has these types of members:</span></span>

-   [<span data-ttu-id="64056-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="64056-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="64056-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="64056-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="64056-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="64056-112">Methods</span></span>

<span data-ttu-id="64056-113">L’objet **Record** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="64056-113">The **Record** object has these methods.</span></span>



| <span data-ttu-id="64056-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="64056-114">Method</span></span>                                  | <span data-ttu-id="64056-115">Description</span><span class="sxs-lookup"><span data-stu-id="64056-115">Description</span></span>                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64056-116">**ClearData**</span><span class="sxs-lookup"><span data-stu-id="64056-116">**ClearData**</span></span>](record-cleardata.md)   | <span data-ttu-id="64056-117">Efface les données de tous les champs, en leur affectant la valeur null.</span><span class="sxs-lookup"><span data-stu-id="64056-117">Clears the data in all fields, setting them to null.</span></span><br/>                                      |
| [<span data-ttu-id="64056-118">**FormatText**</span><span class="sxs-lookup"><span data-stu-id="64056-118">**FormatText**</span></span>](record-formattext.md) | <span data-ttu-id="64056-119">Met en forme les champs en fonction du modèle dans le champ 0.</span><span class="sxs-lookup"><span data-stu-id="64056-119">Formats fields according to the template in field 0.</span></span><br/>                                      |
| [<span data-ttu-id="64056-120">**ReadStream**</span><span class="sxs-lookup"><span data-stu-id="64056-120">**ReadStream**</span></span>](record-readstream.md) | <span data-ttu-id="64056-121">Lit un nombre spécifié d’octets à partir d’un champ d’enregistrement contenant les données de flux.</span><span class="sxs-lookup"><span data-stu-id="64056-121">Reads a specified number of bytes from a record field holding stream data.</span></span><br/>                |
| [<span data-ttu-id="64056-122">**SetStream**</span><span class="sxs-lookup"><span data-stu-id="64056-122">**SetStream**</span></span>](record-setstream.md)   | <span data-ttu-id="64056-123">Copie le contenu du fichier spécifié dans le champ d’enregistrement désigné en tant que données de flux.</span><span class="sxs-lookup"><span data-stu-id="64056-123">Copies the content of the specified file into the designated record field as stream data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="64056-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="64056-124">Properties</span></span>

<span data-ttu-id="64056-125">L’objet **Record** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="64056-125">The **Record** object has these properties.</span></span>



| <span data-ttu-id="64056-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="64056-126">Property</span></span>                                             | <span data-ttu-id="64056-127">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="64056-127">Access type</span></span>           | <span data-ttu-id="64056-128">Description</span><span class="sxs-lookup"><span data-stu-id="64056-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64056-129">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="64056-129">**DataSize**</span></span>](record-datasize.md)<br/>       |                       | <span data-ttu-id="64056-130">Retourne la taille des données pour le champ désigné.</span><span class="sxs-lookup"><span data-stu-id="64056-130">Returns the size of the data for the designated field.</span></span><br/>                             |
| [<span data-ttu-id="64056-131">**FieldCount**</span><span class="sxs-lookup"><span data-stu-id="64056-131">**FieldCount**</span></span>](record-fieldcount.md)<br/>   |                       | <span data-ttu-id="64056-132">Retourne le nombre de champs dans l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="64056-132">Returns the number of fields in the record.</span></span><br/>                                        |
| [<span data-ttu-id="64056-133">**IntegerData**</span><span class="sxs-lookup"><span data-stu-id="64056-133">**IntegerData**</span></span>](record-integerdata.md)<br/> | <span data-ttu-id="64056-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="64056-134">Read/write</span></span><br/> | <span data-ttu-id="64056-135">Transfère les données de type entier 32 bits dans ou en dehors d’un champ spécifié dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="64056-135">Transfers 32-bit integer data in to or out of a specified field within the record.</span></span><br/> |
| [<span data-ttu-id="64056-136">**IsNull**</span><span class="sxs-lookup"><span data-stu-id="64056-136">**IsNull**</span></span>](record-isnull.md)<br/>           |                       | <span data-ttu-id="64056-137">Retourne la valeur true si le champ indiqué est null et false si le champ contient des données.</span><span class="sxs-lookup"><span data-stu-id="64056-137">Returns True if the indicated field is null and False if the field contains data.</span></span><br/>  |
| [<span data-ttu-id="64056-138">**StringData**</span><span class="sxs-lookup"><span data-stu-id="64056-138">**StringData**</span></span>](record-stringdata.md)<br/>   | <span data-ttu-id="64056-139">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="64056-139">Read/write</span></span><br/> | <span data-ttu-id="64056-140">Transfère les données de chaîne dans ou en dehors d’un champ spécifié dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="64056-140">Transfers string data in to or out of a specified field within the record.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="64056-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64056-141">Requirements</span></span>



| <span data-ttu-id="64056-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64056-142">Requirement</span></span> | <span data-ttu-id="64056-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="64056-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64056-144">Version</span><span class="sxs-lookup"><span data-stu-id="64056-144">Version</span></span><br/> | <span data-ttu-id="64056-145">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="64056-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="64056-146">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="64056-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="64056-147">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="64056-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="64056-148">DLL</span><span class="sxs-lookup"><span data-stu-id="64056-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="64056-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64056-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="64056-150">IID</span><span class="sxs-lookup"><span data-stu-id="64056-150">IID</span></span><br/>     | <span data-ttu-id="64056-151">IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="64056-151">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="64056-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64056-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64056-153">**Méthode CreateRecord**</span><span class="sxs-lookup"><span data-stu-id="64056-153">**CreateRecord Method**</span></span>](installer-createrecord.md)
</dt> <dt>

[<span data-ttu-id="64056-154">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="64056-154">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




