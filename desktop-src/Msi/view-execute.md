---
description: La méthode Execute de l’objet View utilise le jeton de point d’interrogation pour représenter les paramètres dans une instruction SQL. Pour plus d’informations, consultez syntaxe SQL. Les valeurs de ces paramètres sont transmises en tant que champs correspondants d’un enregistrement de paramètre.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: Méthode de View.Exe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525141"
---
# <a name="viewexecute-method"></a><span data-ttu-id="bc42a-105">Méthode de View.Exe</span><span class="sxs-lookup"><span data-stu-id="bc42a-105">View.Execute method</span></span>

<span data-ttu-id="bc42a-106">La méthode **Execute** de l’objet [**View**](view-object.md) utilise le jeton de point d’interrogation pour représenter les paramètres dans une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="bc42a-106">The **Execute** method of the [**View**](view-object.md) object uses the question mark token to represent parameters in an SQL statement.</span></span> <span data-ttu-id="bc42a-107">Pour plus d’informations, consultez [syntaxe SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="bc42a-107">For more information, see [SQL Syntax](sql-syntax.md).</span></span> <span data-ttu-id="bc42a-108">Les valeurs de ces paramètres sont transmises en tant que champs correspondants d’un enregistrement de paramètre.</span><span class="sxs-lookup"><span data-stu-id="bc42a-108">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc42a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc42a-109">Syntax</span></span>


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="bc42a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc42a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc42a-111">*enregistrement*</span><span class="sxs-lookup"><span data-stu-id="bc42a-111">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="bc42a-112">Objets d' [**enregistrement**](record-object.md) facultatifs qui contiennent les valeurs qui remplacent les jetons de paramètre ( ?) dans la requête SQL.</span><span class="sxs-lookup"><span data-stu-id="bc42a-112">Optional [**Record**](record-object.md) objects that contains the values that replace the parameter tokens (?) in the SQL query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc42a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc42a-113">Return value</span></span>

<span data-ttu-id="bc42a-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bc42a-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc42a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bc42a-115">Remarks</span></span>

<span data-ttu-id="bc42a-116">Cette méthode doit être appelée avant tout appel à la méthode [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="bc42a-116">This method must be called before any calls to the [**Fetch**](view-fetch.md) method.</span></span>

<span data-ttu-id="bc42a-117">Si la requête SQL spécifie des valeurs avec des marqueurs de paramètres ( ?), un enregistrement qui contient toutes les valeurs de remplacement doit être dans le même ordre et le même type de données que les marqueurs de paramètres.</span><span class="sxs-lookup"><span data-stu-id="bc42a-117">If the SQL query specifies values with parameter markers (?), a record must be supplied that contains all of the replacement values, which must be in the same order and of the same data type as the parameter markers.</span></span> <span data-ttu-id="bc42a-118">Lorsque cette méthode est utilisée avec les requêtes INSERT et UPDATE, les jetons de point d’interrogation doivent précéder toutes les valeurs non paramétrées.</span><span class="sxs-lookup"><span data-stu-id="bc42a-118">When this method is used with INSERT and UPDATE queries, the question mark tokens must precede all the non-parameterized values.</span></span>

<span data-ttu-id="bc42a-119">Par exemple, ces requêtes sont valides :</span><span class="sxs-lookup"><span data-stu-id="bc42a-119">For example, these queries are valid:</span></span>

<span data-ttu-id="bc42a-120">MISE à jour {table-List} définie {Column} = ?</span><span class="sxs-lookup"><span data-stu-id="bc42a-120">UPDATE {table-list} SET {column}= ?</span></span> <span data-ttu-id="bc42a-121">, {Column} = {constant}</span><span class="sxs-lookup"><span data-stu-id="bc42a-121">, {column}= {constant}</span></span>

<span data-ttu-id="bc42a-122">INSÉRER dans {table} ({Column-List}) valeurs ( ?, {constant-List})</span><span class="sxs-lookup"><span data-stu-id="bc42a-122">INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})</span></span>

<span data-ttu-id="bc42a-123">Toutefois, ces requêtes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="bc42a-123">However these queries are invalid:</span></span>

<span data-ttu-id="bc42a-124">UPDATE {table-List} SET {Column} = {constante}, {Column} = ?</span><span class="sxs-lookup"><span data-stu-id="bc42a-124">UPDATE {table-list} SET {column}= {constant}, {column}=?</span></span>

<span data-ttu-id="bc42a-125">INSÉRER dans {table} ({Column-List}) valeurs ({constant-List}, ?</span><span class="sxs-lookup"><span data-stu-id="bc42a-125">INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ?</span></span> <span data-ttu-id="bc42a-126">)</span><span class="sxs-lookup"><span data-stu-id="bc42a-126">)</span></span>

<span data-ttu-id="bc42a-127">Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="bc42a-127">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc42a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc42a-128">Requirements</span></span>



| <span data-ttu-id="bc42a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc42a-129">Requirement</span></span> | <span data-ttu-id="bc42a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc42a-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc42a-131">Version</span><span class="sxs-lookup"><span data-stu-id="bc42a-131">Version</span></span><br/> | <span data-ttu-id="bc42a-132">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bc42a-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bc42a-133">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bc42a-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bc42a-134">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="bc42a-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bc42a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bc42a-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="bc42a-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc42a-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bc42a-137">IID</span><span class="sxs-lookup"><span data-stu-id="bc42a-137">IID</span></span><br/>     | <span data-ttu-id="bc42a-138">L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bc42a-138">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




