---
description: La propriété ColumnInfo de l’objet View retourne un objet record contenant les informations demandées sur chaque colonne du jeu de résultats.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: View. ColumnInfo, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 38c016b15108446cc04114adc06ad12686d9932c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539631"
---
# <a name="viewcolumninfo-property"></a><span data-ttu-id="b5db7-103">View. ColumnInfo, propriété</span><span class="sxs-lookup"><span data-stu-id="b5db7-103">View.ColumnInfo property</span></span>

<span data-ttu-id="b5db7-104">La propriété **COLUMNINFO** de l’objet [**View**](view-object.md) retourne un objet [**Record**](record-object.md) contenant les informations demandées sur chaque colonne du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="b5db7-104">The **ColumnInfo** property of the [**View**](view-object.md) object returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span> <span data-ttu-id="b5db7-105">Les noms de colonnes ou les définitions de colonne peuvent être demandés.</span><span class="sxs-lookup"><span data-stu-id="b5db7-105">Either the column names or the column definitions may be requested.</span></span> <span data-ttu-id="b5db7-106">Les constantes fournies dans la liste de sélection n’ont pas de noms.</span><span class="sxs-lookup"><span data-stu-id="b5db7-106">Constants supplied in the Select list do not have names.</span></span>

<span data-ttu-id="b5db7-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b5db7-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5db7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5db7-108">Syntax</span></span>


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a><span data-ttu-id="b5db7-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b5db7-109">Property value</span></span>

<span data-ttu-id="b5db7-110">Informations requises pour chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="b5db7-110">Required information needed for each column.</span></span>



| <span data-ttu-id="b5db7-111">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="b5db7-111">Parameter name</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="b5db7-112">Signification</span><span class="sxs-lookup"><span data-stu-id="b5db7-112">Meaning</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <span data-ttu-id="b5db7-113"><dt>**msiColumnInfoNames**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b5db7-113"><dt>**msiColumnInfoNames**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="b5db7-114">Retourne les noms de toutes les colonnes non constantes dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="b5db7-114">Returns the names of all nonconstant columns in result set.</span></span><br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <span data-ttu-id="b5db7-115"><dt>**msiColumnInfoTypes**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b5db7-115"><dt>**msiColumnInfoTypes**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="b5db7-116">Retourne les types de toutes les colonnes non constantes dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="b5db7-116">Returns the types of all nonconstant columns in result set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b5db7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b5db7-117">Remarks</span></span>

<span data-ttu-id="b5db7-118">Les descriptions de colonne retournées par la propriété **COLUMNINFO** sont au format décrit dans [format de définition de colonne](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="b5db7-118">The column descriptions returned by the **ColumnInfo** property are in the format described in [Column Definition Format](column-definition-format.md).</span></span> <span data-ttu-id="b5db7-119">Chaque colonne est décrite par une chaîne dans le champ d’enregistrement correspondant.</span><span class="sxs-lookup"><span data-stu-id="b5db7-119">Each column is described by a string in the corresponding record field.</span></span> <span data-ttu-id="b5db7-120">La chaîne de définition se compose d’une seule lettre représentant le type de données suivi de la largeur de la colonne (en caractères, le cas échéant, ou d’octets).</span><span class="sxs-lookup"><span data-stu-id="b5db7-120">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, or else bytes).</span></span> <span data-ttu-id="b5db7-121">Une largeur de zéro désigne une largeur illimitée (champs de texte long et flux).</span><span class="sxs-lookup"><span data-stu-id="b5db7-121">A width of zero designates an unbounded width (long text fields and streams).</span></span> <span data-ttu-id="b5db7-122">Une lettre majuscule indique que les valeurs NULL sont autorisées dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="b5db7-122">An uppercase letter indicates that Null values are allowed in the column.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5db7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5db7-123">Requirements</span></span>



| <span data-ttu-id="b5db7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5db7-124">Requirement</span></span> | <span data-ttu-id="b5db7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5db7-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5db7-126">Version</span><span class="sxs-lookup"><span data-stu-id="b5db7-126">Version</span></span><br/> | <span data-ttu-id="b5db7-127">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b5db7-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b5db7-128">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b5db7-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b5db7-129">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5db7-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b5db7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b5db7-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5db7-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5db7-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b5db7-132">IID</span><span class="sxs-lookup"><span data-stu-id="b5db7-132">IID</span></span><br/>     | <span data-ttu-id="b5db7-133">L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b5db7-133">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




