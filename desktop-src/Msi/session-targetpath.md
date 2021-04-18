---
description: La propriété TargetPath de l’objet session est une propriété en lecture-écriture qui fournit le chemin d’accès complet au dossier désigné sur le lecteur cible de l’installation.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Session. TargetPath, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533470"
---
# <a name="sessiontargetpath-property"></a><span data-ttu-id="ea03e-103">Session. TargetPath, propriété</span><span class="sxs-lookup"><span data-stu-id="ea03e-103">Session.TargetPath property</span></span>

<span data-ttu-id="ea03e-104">La propriété **targetPath** de l’objet [**session**](session-object.md) est une propriété en lecture-écriture qui fournit le chemin d’accès complet au dossier désigné sur le lecteur cible de l’installation.</span><span class="sxs-lookup"><span data-stu-id="ea03e-104">The **TargetPath** property of the [**Session**](session-object.md) object is a read-write property that provides the full path to the designated folder on the installation target drive.</span></span>

<span data-ttu-id="ea03e-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ea03e-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea03e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea03e-106">Syntax</span></span>


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a><span data-ttu-id="ea03e-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ea03e-107">Property value</span></span>

<span data-ttu-id="ea03e-108">Nom d’une propriété de dossier obligatoire et sensible à la casse, comme spécifié par une clé primaire de la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="ea03e-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="ea03e-109">Une erreur est générée si le dossier n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="ea03e-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea03e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ea03e-110">Remarks</span></span>

<span data-ttu-id="ea03e-111">N’essayez pas de configurer le chemin d’accès cible si les composants qui utilisent ces chemins d’accès sont déjà installés pour l’utilisateur actuel ou pour un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ea03e-111">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="ea03e-112">Vérifiez la propriété [**ProductState**](productstate.md) pour déterminer si le produit qui contient le composant est installé.</span><span class="sxs-lookup"><span data-stu-id="ea03e-112">Check the [**ProductState**](productstate.md) property to determine if the product that contains the component is installed.</span></span>

<span data-ttu-id="ea03e-113">Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="ea03e-113">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea03e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea03e-114">Requirements</span></span>



| <span data-ttu-id="ea03e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea03e-115">Requirement</span></span> | <span data-ttu-id="ea03e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea03e-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea03e-117">Version</span><span class="sxs-lookup"><span data-stu-id="ea03e-117">Version</span></span><br/> | <span data-ttu-id="ea03e-118">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ea03e-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ea03e-119">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ea03e-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ea03e-120">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="ea03e-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ea03e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ea03e-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="ea03e-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea03e-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ea03e-123">IID</span><span class="sxs-lookup"><span data-stu-id="ea03e-123">IID</span></span><br/>     | <span data-ttu-id="ea03e-124">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ea03e-124">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




