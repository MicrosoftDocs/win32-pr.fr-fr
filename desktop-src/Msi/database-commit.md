---
description: La méthode Commit de l’objet Database finalise la forme persistante de la base de données.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Database. Commit, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543293"
---
# <a name="databasecommit-method"></a><span data-ttu-id="a8e1f-103">Database. Commit, méthode</span><span class="sxs-lookup"><span data-stu-id="a8e1f-103">Database.Commit method</span></span>

<span data-ttu-id="a8e1f-104">La méthode **Commit** de l’objet [**Database**](database-object.md) finalise la forme persistante de la base de données.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-104">The **Commit** method of the [**Database**](database-object.md) object finalizes the persistent form of the database.</span></span> <span data-ttu-id="a8e1f-105">Toutes les données persistantes sont écrites dans la base de données accessible en écriture et aucune colonne ou ligne temporaire n’est écrite.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-105">All persistent data is written to the writeable database, and no temporary columns or rows are written.</span></span> <span data-ttu-id="a8e1f-106">Cette méthode n’a aucun effet sur une base de données ouverte en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-106">This method has no effect on a database opened as read-only.</span></span> <span data-ttu-id="a8e1f-107">Cette méthode peut être appelée plusieurs fois pour enregistrer l’état actuel des tables chargées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-107">This method can be called multiple times to save the current state of tables loaded into memory.</span></span> <span data-ttu-id="a8e1f-108">Lorsque la base de données est fermée, toutes les modifications apportées après la dernière **validation** sont annulées.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-108">When the database is finally closed, any changes made subsequent to the last **Commit** are rolled back.</span></span> <span data-ttu-id="a8e1f-109">Cette méthode est normalement appelée avant l’arrêt lorsque toutes les modifications de la base de données ont été finalisées.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-109">This method is normally called prior to shutdown when all database changes have been finalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e1f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8e1f-110">Syntax</span></span>


```JScript
Database.Commit()
```



## <a name="parameters"></a><span data-ttu-id="a8e1f-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8e1f-111">Parameters</span></span>

<span data-ttu-id="a8e1f-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8e1f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8e1f-113">Return value</span></span>

<span data-ttu-id="a8e1f-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8e1f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a8e1f-115">Remarks</span></span>

<span data-ttu-id="a8e1f-116">Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e1f-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8e1f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8e1f-117">Requirements</span></span>



| <span data-ttu-id="a8e1f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8e1f-118">Requirement</span></span> | <span data-ttu-id="a8e1f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8e1f-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e1f-120">Version</span><span class="sxs-lookup"><span data-stu-id="a8e1f-120">Version</span></span><br/> | <span data-ttu-id="a8e1f-121">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a8e1f-122">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a8e1f-123">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8e1f-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a8e1f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a8e1f-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="a8e1f-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8e1f-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a8e1f-126">IID</span><span class="sxs-lookup"><span data-stu-id="a8e1f-126">IID</span></span><br/>     | <span data-ttu-id="a8e1f-127">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a8e1f-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




