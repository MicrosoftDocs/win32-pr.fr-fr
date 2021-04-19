---
description: La propriété PrimaryKeys de l’objet de base de données retourne un objet record contenant le nom de la table dans le champ 0 et les noms de colonnes (qui composent les clés primaires) dans les champs suivants qui correspondent à leurs numéros de colonne.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Propriété Database. PrimaryKeys
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532013"
---
# <a name="databaseprimarykeys-property"></a><span data-ttu-id="2ee5a-103">Propriété Database. PrimaryKeys</span><span class="sxs-lookup"><span data-stu-id="2ee5a-103">Database.PrimaryKeys property</span></span>

<span data-ttu-id="2ee5a-104">La propriété **PrimaryKeys** de l’objet [**de base de données**](database-object.md) retourne un objet [**Record**](record-object.md) contenant le nom de la table dans le champ 0 et les noms de colonnes (qui composent les clés primaires) dans les champs suivants qui correspondent à leurs numéros de colonne.</span><span class="sxs-lookup"><span data-stu-id="2ee5a-104">The **PrimaryKeys** property of the [**Database**](database-object.md) object returns a [**Record**](record-object.md) object containing the table name in field 0 and the column names (comprising the primary keys) in succeeding fields corresponding to their column numbers.</span></span> <span data-ttu-id="2ee5a-105">Le nombre de champs de l’enregistrement est le nombre de colonnes clés primaires.</span><span class="sxs-lookup"><span data-stu-id="2ee5a-105">The field count of the record is the count of primary key columns.</span></span>

<span data-ttu-id="2ee5a-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2ee5a-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ee5a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ee5a-107">Syntax</span></span>


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a><span data-ttu-id="2ee5a-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2ee5a-108">Property value</span></span>

<span data-ttu-id="2ee5a-109">Nom obligatoire d’une table existante.</span><span class="sxs-lookup"><span data-stu-id="2ee5a-109">Required name of an existing table.</span></span> <span data-ttu-id="2ee5a-110">Une erreur est générée si la table n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="2ee5a-110">An error is generated if the table does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ee5a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2ee5a-111">Remarks</span></span>

<span data-ttu-id="2ee5a-112">La propriété **PrimaryKeys** ne peut pas être utilisée avec la table [ \_ tables](-tables-table.md) ou la [ \_ Table Columns](-columns-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ee5a-112">The **PrimaryKeys** property cannot be used with the [\_Tables table](-tables-table.md) or the [\_Columns table](-columns-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ee5a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ee5a-113">Requirements</span></span>



| <span data-ttu-id="2ee5a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ee5a-114">Requirement</span></span> | <span data-ttu-id="2ee5a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ee5a-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee5a-116">Version</span><span class="sxs-lookup"><span data-stu-id="2ee5a-116">Version</span></span><br/> | <span data-ttu-id="2ee5a-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2ee5a-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2ee5a-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2ee5a-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2ee5a-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="2ee5a-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2ee5a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2ee5a-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="2ee5a-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5a-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2ee5a-122">IID</span><span class="sxs-lookup"><span data-stu-id="2ee5a-122">IID</span></span><br/>     | <span data-ttu-id="2ee5a-123">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2ee5a-123">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




