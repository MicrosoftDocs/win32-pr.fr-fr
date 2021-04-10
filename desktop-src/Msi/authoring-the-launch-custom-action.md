---
description: Le code source d’un exemple d’action personnalisée nommé Launch, qui répond aux exemples de spécifications, est fourni par le kit de développement logiciel (SDK) Windows Installer en tant que fichier Tutorial. cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Création de l’action personnalisée de lancement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951755"
---
# <a name="authoring-the-launch-custom-action"></a><span data-ttu-id="3e301-103">Création de l’action personnalisée de lancement</span><span class="sxs-lookup"><span data-stu-id="3e301-103">Authoring the Launch Custom Action</span></span>

<span data-ttu-id="3e301-104">Le code source d’un exemple d’action personnalisée nommé Launch, qui répond aux exemples de spécifications, est fourni par le kit de développement logiciel (SDK) Windows Installer en tant que fichier Tutorial. cpp.</span><span class="sxs-lookup"><span data-stu-id="3e301-104">The source code for a sample custom action named Launch, which meets the sample specifications, is provided by the Windows Installer SDK as the file Tutorial.cpp.</span></span> <span data-ttu-id="3e301-105">Cette action personnalisée utilise [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) pour mettre en forme une chaîne contenant des propriétés.</span><span class="sxs-lookup"><span data-stu-id="3e301-105">This custom action makes use of [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) to format a string containing properties.</span></span> <span data-ttu-id="3e301-106">La propriété \[ \# FileKey \] correspond au chemin d’accès complet du fichier html.</span><span class="sxs-lookup"><span data-stu-id="3e301-106">The property \[\#FileKey\] resolves to the full path of the HTML file.</span></span> <span data-ttu-id="3e301-107">Utilisez le fichier source pour créer le fichier Tutorial.dll.</span><span class="sxs-lookup"><span data-stu-id="3e301-107">Use the source file to create the file Tutorial.dll.</span></span> <span data-ttu-id="3e301-108">Le point d’entrée de cette DLL est LaunchTutorial.</span><span class="sxs-lookup"><span data-stu-id="3e301-108">The entry point to this DLL is LaunchTutorial.</span></span>

<span data-ttu-id="3e301-109">L’exemple d’action personnalisée Launch appelle une DLL écrite en C++ et est générée à partir d’un flux binaire temporaire.</span><span class="sxs-lookup"><span data-stu-id="3e301-109">The sample custom action Launch calls a DLL written in C++ and is generated from a temporary binary stream.</span></span> <span data-ttu-id="3e301-110">Les actions personnalisées de ce type incluent les constantes de type de base msidbCustomActionTypeDll et msidbCustomActionTypeBinaryData, qui donnent un type numérique de base égal à 1.</span><span class="sxs-lookup"><span data-stu-id="3e301-110">Custom actions of this type include the base type constants msidbCustomActionTypeDll and msidbCustomActionTypeBinaryData, which give a base numeric type equal to 1.</span></span> <span data-ttu-id="3e301-111">Consultez [type d’action personnalisée 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="3e301-111">See [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="3e301-112">Étant donné que les spécifications requièrent que l’installation se poursuive en cas d’échec de l’action personnalisée, Launch comprend également la constante facultative **msidbCustomActionTypeContinue**, qui est 64.</span><span class="sxs-lookup"><span data-stu-id="3e301-112">Because the specifications require that the installation continue if the custom action fails, Launch also includes the optional constant **msidbCustomActionTypeContinue**, which is 64.</span></span> <span data-ttu-id="3e301-113">Consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="3e301-113">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span> <span data-ttu-id="3e301-114">Le type numérique total du lancement est 65.</span><span class="sxs-lookup"><span data-stu-id="3e301-114">The total numeric type of Launch is 65.</span></span>

<span data-ttu-id="3e301-115">Continuez à [Ajouter le lancement aux tables CustomAction et binaires](adding-launch-to-the-customaction-and-binary-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3e301-115">Continue to [Adding Launch to the CustomAction and Binary Tables](adding-launch-to-the-customaction-and-binary-tables.md).</span></span>

 

 



