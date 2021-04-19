---
description: La propriété TARGETDIR spécifie le répertoire de destination racine pour l’installation.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: TARGETDIR, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544103"
---
# <a name="targetdir-property"></a><span data-ttu-id="ed463-103">TARGETDIR, propriété</span><span class="sxs-lookup"><span data-stu-id="ed463-103">TARGETDIR property</span></span>

<span data-ttu-id="ed463-104">La propriété **targetDir** spécifie le répertoire de destination racine pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="ed463-104">The **TARGETDIR** property specifies the root destination directory for the installation.</span></span> <span data-ttu-id="ed463-105">**TargetDir** doit être le nom d’une racine dans la table [Directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ed463-105">**TARGETDIR** must be the name of one root in the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="ed463-106">Il ne peut y avoir qu’un seul répertoire de destination racine.</span><span class="sxs-lookup"><span data-stu-id="ed463-106">There may be only a single root destination directory.</span></span> <span data-ttu-id="ed463-107">Au cours d’une [installation administrative](administrative-installation.md) , cette propriété spécifie l’emplacement de copie du package d’installation.</span><span class="sxs-lookup"><span data-stu-id="ed463-107">During an [administrative installation](administrative-installation.md) this property specifies the location to copy the installation package.</span></span> <span data-ttu-id="ed463-108">Au cours d’une installation non administrative, cette propriété spécifie le répertoire de destination racine.</span><span class="sxs-lookup"><span data-stu-id="ed463-108">During a non-administrative installation this property specifies the root destination directory.</span></span>

<span data-ttu-id="ed463-109">Pour spécifier le répertoire de destination racine, définissez la colonne Directory de la table Directory sur la propriété **targetDir** et la colonne DefaultDir sur la propriété [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="ed463-109">To specify the root destination directory, set the Directory column of the Directory table to the **TARGETDIR** property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="ed463-110">Si la propriété **targetDir** est définie, le répertoire de destination est résolu à la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="ed463-110">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="ed463-111">Si la propriété **targetDir** n’est pas définie, la propriété [**ROOTDRIVE**](rootdrive.md) est utilisée pour résoudre le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="ed463-111">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span> <span data-ttu-id="ed463-112">Pour plus d’informations sur l’utilisation de la propriété **targetDir** , consultez [utilisation de la table Directory](using-the-directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="ed463-112">For more information about using the **TARGETDIR** property, see [Using the Directory Table](using-the-directory-table.md).</span></span>

<span data-ttu-id="ed463-113">Notez que la valeur de la propriété **targetDir** est généralement définie au niveau de la ligne de commande ou par le biais d’une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed463-113">Note that the value of the **TARGETDIR** property is typically set at the command line or through a user interface.</span></span> <span data-ttu-id="ed463-114">La définition de **targetDir** en créant un chemin dans la [table de propriétés](property-table.md) n’est pas recommandée, car les ordinateurs diffèrent dans la configuration du lecteur local.</span><span class="sxs-lookup"><span data-stu-id="ed463-114">Setting **TARGETDIR** by authoring a path into the [Property table](property-table.md) is not recommended because computers differ in the set up of the local drive.</span></span>

<span data-ttu-id="ed463-115">Pour plus d’informations sur la modification de TARGETDIR pendant une installation, consultez [modification de l’emplacement cible d’un répertoire](changing-the-target-location-for-a-directory.md)</span><span class="sxs-lookup"><span data-stu-id="ed463-115">For more information on how to change TARGETDIR during an installation see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="ed463-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed463-116">Requirements</span></span>



| <span data-ttu-id="ed463-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed463-117">Requirement</span></span> | <span data-ttu-id="ed463-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed463-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed463-119">Version</span><span class="sxs-lookup"><span data-stu-id="ed463-119">Version</span></span><br/> | <span data-ttu-id="ed463-120">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ed463-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ed463-121">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed463-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ed463-122">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed463-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ed463-123">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ed463-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed463-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed463-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed463-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ed463-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




