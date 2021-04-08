---
description: ICE83 valide la table MsiAssembly.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ac38b4455875314c85fa08c1cfdc329e0cb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034399"
---
# <a name="ice83"></a><span data-ttu-id="52aa1-103">ICE83</span><span class="sxs-lookup"><span data-stu-id="52aa1-103">ICE83</span></span>

<span data-ttu-id="52aa1-104">ICE83 valide la [table MsiAssembly](msiassembly-table.md).</span><span class="sxs-lookup"><span data-stu-id="52aa1-104">ICE83 validates the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="52aa1-105">Cette action personnalisée ICE publie une erreur si le chemin d’accès de la clé pour un composant contenant un assembly Win32 est défini sur le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="52aa1-105">This ICE custom action posts an error if the key path for a component containing a Win32 assembly is set to the manifest file.</span></span> <span data-ttu-id="52aa1-106">Explicitement, l’erreur est publiée si la valeur entrée dans le champ keyPath de la [table Component](component-table.md) est égale à la valeur entrée dans le \_ champ manifeste de fichier de la table MsiAssembly.</span><span class="sxs-lookup"><span data-stu-id="52aa1-106">Explicitly the error is posted if the value entered in the KeyPath field of the [Component table](component-table.md) equals the value entered in the File\_Manifest field of the MsiAssembly table.</span></span> <span data-ttu-id="52aa1-107">Cette action personnalisée ICE publie une erreur s’il existe au moins un enregistrement dans la table MsiAssembly et que la [table InstallExecuteSequence](installexecutesequence-table.md) ne contient pas à la fois l’action [MsiPublishAssemblies](msipublishassemblies-action.md) et l' [action MsiUnpublishAssemblies](msiunpublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="52aa1-107">This ICE custom action posts an error if there is at least one record in the MsiAssembly table and the [InstallExecuteSequence table](installexecutesequence-table.md) does not contain both the [MsiPublishAssemblies Action](msipublishassemblies-action.md) and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

## <a name="result"></a><span data-ttu-id="52aa1-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="52aa1-108">Result</span></span>

<span data-ttu-id="52aa1-109">ICE83 publie les erreurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="52aa1-109">ICE83 posts the following errors.</span></span>



| <span data-ttu-id="52aa1-110">Erreur ICE83</span><span class="sxs-lookup"><span data-stu-id="52aa1-110">ICE83 error</span></span>                                                                                                   | <span data-ttu-id="52aa1-111">Description</span><span class="sxs-lookup"><span data-stu-id="52aa1-111">Description</span></span>                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52aa1-112">Le chemin d’accès de la clé de l’assembly SxS Win32 (composant \_ = \[ 1 \] ) ne doit pas être son fichier manifeste</span><span class="sxs-lookup"><span data-stu-id="52aa1-112">The key path for Win32 SXS Assembly (Component\_=\[1\]) SHOULD NOT be its manifest file</span></span>                       | <span data-ttu-id="52aa1-113">ICE83 publie cette erreur quand le champ keyPath d’un assembly Win32 a pour valeur son fichier manifeste (composant. keyPath = = MsiAssembly. file \_ manifest).</span><span class="sxs-lookup"><span data-stu-id="52aa1-113">ICE83 posts this error when the KeyPath field for a Win32 Assembly is set to its manifest file (Component.KeyPath == MsiAssembly.File\_Manifest).</span></span> <span data-ttu-id="52aa1-114">\[1 \] est le keyPath dans la table des composants</span><span class="sxs-lookup"><span data-stu-id="52aa1-114">\[1\] is KeyPath in Component table</span></span>                          |
| <span data-ttu-id="52aa1-115">Les actions MsiPublishAssemblies et MsiUnpublishAssemblies doivent être présentes dans la table InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="52aa1-115">Both MsiPublishAssemblies AND MsiUnpublishAssemblies actions MUST be present in InstallExecuteSequence table.</span></span> | <span data-ttu-id="52aa1-116">ICE83 publie cette erreur lorsqu’il existe au moins une entrée dans la table MsiAssembly, mais que la table InstallExecuteSequence ne contient pas à la fois l’action MsiAssemblyPublish et l’action MsiAssemblyUnpublish.</span><span class="sxs-lookup"><span data-stu-id="52aa1-116">ICE83 posts this error when there is at least one entry in the MsiAssembly table but the InstallExecuteSequence table does not contain both the MsiAssemblyPublish action and the MsiAssemblyUnpublish action.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="52aa1-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52aa1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52aa1-118">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="52aa1-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



