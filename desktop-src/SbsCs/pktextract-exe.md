---
description: Pktextract.exe est un outil qui extrait l’attribut publicKeyToken à partir d’un fichier de certificat.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd163efabd01d65969788aefc2386b2f49079729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115186"
---
# <a name="pktextractexe"></a><span data-ttu-id="e1df8-103">Pktextract.exe</span><span class="sxs-lookup"><span data-stu-id="e1df8-103">Pktextract.exe</span></span>

<span data-ttu-id="e1df8-104">Pktextract.exe est un outil qui extrait l’attribut **PublicKeyToken** à partir d’un fichier de certificat.</span><span class="sxs-lookup"><span data-stu-id="e1df8-104">Pktextract.exe is a tool that extracts the **publicKeyToken** attribute from a certificate file.</span></span> <span data-ttu-id="e1df8-105">La sortie est **PublicKeyToken**, qui est un identificateur unique de 16 caractères (8 octets) de la clé publique présente dans le certificat, dans un format qui peut être facilement collé dans une instruction d’identité d’assembly.</span><span class="sxs-lookup"><span data-stu-id="e1df8-105">The output is the **publicKeyToken**, which is a unique 16-character (8-byte) identifier of the public key present in the certificate, in a format that can easily be pasted into an assembly identity statement.</span></span> <span data-ttu-id="e1df8-106">Le fichier de certificat doit être présent dans le même répertoire que Pktextract.exe pour pouvoir utiliser l’utilitaire.</span><span class="sxs-lookup"><span data-stu-id="e1df8-106">The certificate file must be present in the same directory as Pktextract.exe to use the utility.</span></span> <span data-ttu-id="e1df8-107">Pktextract.exe est fourni dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e1df8-107">Pktextract.exe is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="e1df8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1df8-108">Syntax</span></span>

<span data-ttu-id="e1df8-109">**pktextract.exe** *<filename. cer>* **\[ -Quiet \] \[ -nologo \]**</span><span class="sxs-lookup"><span data-stu-id="e1df8-109">**pktextract.exe** *<filename.cer>* **\[-quiet\] \[-nologo\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="e1df8-110">Options de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="e1df8-110">Command Line Options</span></span>

<span data-ttu-id="e1df8-111">Pktextract.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="e1df8-111">Pktextract.exe uses the following case-insensitive command line options.</span></span>



| <span data-ttu-id="e1df8-112">Option</span><span class="sxs-lookup"><span data-stu-id="e1df8-112">Option</span></span>  | <span data-ttu-id="e1df8-113">Description</span><span class="sxs-lookup"><span data-stu-id="e1df8-113">Description</span></span>                                                          |
|---------|----------------------------------------------------------------------|
| <span data-ttu-id="e1df8-114">-quiet</span><span class="sxs-lookup"><span data-stu-id="e1df8-114">-quiet</span></span>  | <span data-ttu-id="e1df8-115">Supprime l’affichage complet des informations de certificat.</span><span class="sxs-lookup"><span data-stu-id="e1df8-115">Suppresses full display of certificate information.</span></span> <span data-ttu-id="e1df8-116">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e1df8-116">Optional.</span></span>        |
| <span data-ttu-id="e1df8-117">-nologo</span><span class="sxs-lookup"><span data-stu-id="e1df8-117">-nologo</span></span> | <span data-ttu-id="e1df8-118">S’exécute sans afficher les données de copyright Microsoft standard.</span><span class="sxs-lookup"><span data-stu-id="e1df8-118">Runs without displaying standard Microsoft copyright data.</span></span> <span data-ttu-id="e1df8-119">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e1df8-119">Optional.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e1df8-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1df8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1df8-121">Outils de développement d’assembly côte à côte</span><span class="sxs-lookup"><span data-stu-id="e1df8-121">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



