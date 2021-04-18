---
description: La méthode ReadStream de l’objet record lit un nombre spécifié d’octets à partir d’un champ d’enregistrement qui contient des données de flux.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Record. ReadStream, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533094"
---
# <a name="recordreadstream-method"></a><span data-ttu-id="28892-103">Record. ReadStream, méthode</span><span class="sxs-lookup"><span data-stu-id="28892-103">Record.ReadStream method</span></span>

<span data-ttu-id="28892-104">La méthode **ReadStream** de l’objet [**Record**](record-object.md) lit un nombre spécifié d’octets à partir d’un champ d’enregistrement qui contient des données de flux.</span><span class="sxs-lookup"><span data-stu-id="28892-104">The **ReadStream** method of the [**Record**](record-object.md) object reads a specified number of bytes from a record field that contains stream data.</span></span>

## <a name="syntax"></a><span data-ttu-id="28892-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28892-105">Syntax</span></span>


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a><span data-ttu-id="28892-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28892-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28892-107">*case*</span><span class="sxs-lookup"><span data-stu-id="28892-107">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="28892-108">Numéro de champ obligatoire de la valeur dans l’enregistrement, de base 1.</span><span class="sxs-lookup"><span data-stu-id="28892-108">The required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="28892-109">*length*</span><span class="sxs-lookup"><span data-stu-id="28892-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="28892-110">Nombre d’octets requis pour lire à partir du flux.</span><span class="sxs-lookup"><span data-stu-id="28892-110">The required number of bytes to read from the stream.</span></span>

</dd> <dt>

<span data-ttu-id="28892-111">*format*</span><span class="sxs-lookup"><span data-stu-id="28892-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="28892-112">Interprétation et retour requis des octets de données.</span><span class="sxs-lookup"><span data-stu-id="28892-112">Required interpretation and return of the data bytes.</span></span>



| <span data-ttu-id="28892-113">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="28892-113">Parameter name</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="28892-114">Signification</span><span class="sxs-lookup"><span data-stu-id="28892-114">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <span data-ttu-id="28892-115"><dt>**msiReadStreamInteger**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="28892-115"><dt>**msiReadStreamInteger**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="28892-116">Sous la forme d’un entier long, la longueur doit être comprise entre 1 et 4.</span><span class="sxs-lookup"><span data-stu-id="28892-116">As a long integer the length must be 1 to 4.</span></span><br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <span data-ttu-id="28892-117"><dt>**msiReadStreamBytes**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="28892-117"><dt>**msiReadStreamBytes**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="28892-118">Données sous forme de **BSTR**(un octet par caractère).</span><span class="sxs-lookup"><span data-stu-id="28892-118">The data as a **BSTR**—one byte per character.</span></span><br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <span data-ttu-id="28892-119"><dt>**msiReadStreamAnsi**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="28892-119"><dt>**msiReadStreamAnsi**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="28892-120">Octets ANSI traduits en **BSTR** Unicode.</span><span class="sxs-lookup"><span data-stu-id="28892-120">The ANSI bytes translated to a Unicode **BSTR**.</span></span><br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <span data-ttu-id="28892-121"><dt>**msiReadStreamDirect**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="28892-121"><dt>**msiReadStreamDirect**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="28892-122">Paires d’octets qui sont retournées directement sous forme de **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="28892-122">The byte pairs that are returned directly as a **BSTR**.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28892-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28892-123">Return value</span></span>

<span data-ttu-id="28892-124">Cette méthode retourne une chaîne qui contient le nombre demandé d’octets lus à partir d’un champ d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="28892-124">This method returns a string that contains the requested number of bytes read from a record field.</span></span>

## <a name="remarks"></a><span data-ttu-id="28892-125">Notes</span><span class="sxs-lookup"><span data-stu-id="28892-125">Remarks</span></span>

<span data-ttu-id="28892-126">La valeur retournée d’un champ inexistant est une valeur vide.</span><span class="sxs-lookup"><span data-stu-id="28892-126">The returned value of a nonexistent field is an Empty value.</span></span> <span data-ttu-id="28892-127">Si le flux a moins d’octets que le nombre demandé, la chaîne retournée est raccourcie de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="28892-127">If the stream has fewer bytes that the count requested, the returned string is shortened appropriately.</span></span>

<span data-ttu-id="28892-128">Pour obtenir un exemple de cette méthode, consultez [copier le fichier ANSI dans un champ de base de données](copy-ansi-file-into-a-database-field.md).</span><span class="sxs-lookup"><span data-stu-id="28892-128">For an example of this method, see [Copy ANSI File Into a Database Field](copy-ansi-file-into-a-database-field.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28892-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28892-129">Requirements</span></span>



| <span data-ttu-id="28892-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28892-130">Requirement</span></span> | <span data-ttu-id="28892-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="28892-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28892-132">Version</span><span class="sxs-lookup"><span data-stu-id="28892-132">Version</span></span><br/> | <span data-ttu-id="28892-133">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="28892-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="28892-134">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="28892-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="28892-135">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="28892-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="28892-136">DLL</span><span class="sxs-lookup"><span data-stu-id="28892-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="28892-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28892-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="28892-138">IID</span><span class="sxs-lookup"><span data-stu-id="28892-138">IID</span></span><br/>     | <span data-ttu-id="28892-139">IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="28892-139">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




