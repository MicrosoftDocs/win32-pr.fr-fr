---
description: La méthode OpenDatabase de l’objet Merge ouvre une base de données d’installation Windows Installer, située dans un chemin d’accès spécifié, qui doit être fusionnée avec un module.
ms.assetid: 86f168e5-bc76-476d-9757-9b2a21bb9c4b
title: Merge. OpenDatabase, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenDatabase
- IMsmMerge.OpenDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 2e200da6fe3f4913e53d96a237cac2b4d4c9b77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537811"
---
# <a name="mergeopendatabase-method"></a><span data-ttu-id="3c59a-103">Merge. OpenDatabase, méthode</span><span class="sxs-lookup"><span data-stu-id="3c59a-103">Merge.OpenDatabase method</span></span>

<span data-ttu-id="3c59a-104">La méthode **OpenDatabase** de l’objet [**Merge**](merge-object.md) ouvre une base de données d’installation Windows Installer, située dans un chemin d’accès spécifié, qui doit être fusionnée avec un module.</span><span class="sxs-lookup"><span data-stu-id="3c59a-104">The **OpenDatabase** method of the [**Merge**](merge-object.md) object opens a Windows Installer installation database, located at a specified path, that is to be merged with a module.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c59a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c59a-105">Syntax</span></span>


```JScript
Merge.OpenDatabase(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="3c59a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c59a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c59a-107">*Chemin d’accès*</span><span class="sxs-lookup"><span data-stu-id="3c59a-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="3c59a-108">Chemin d’accès à la base de données en cours d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="3c59a-108">Path to the database being opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c59a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c59a-109">Return value</span></span>

<span data-ttu-id="3c59a-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3c59a-110">This method does not return a value.</span></span>

## <a name="c"></a><span data-ttu-id="3c59a-111">C++</span><span class="sxs-lookup"><span data-stu-id="3c59a-111">C++</span></span>

<span data-ttu-id="3c59a-112">Consultez fonction [**OpenDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-opendatabase) .</span><span class="sxs-lookup"><span data-stu-id="3c59a-112">See [**OpenDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-opendatabase) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c59a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c59a-113">Requirements</span></span>



| <span data-ttu-id="3c59a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c59a-114">Requirement</span></span> | <span data-ttu-id="3c59a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c59a-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c59a-116">Version</span><span class="sxs-lookup"><span data-stu-id="3c59a-116">Version</span></span><br/> | <span data-ttu-id="3c59a-117">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3c59a-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="3c59a-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c59a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3c59a-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c59a-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c59a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3c59a-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="3c59a-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c59a-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
