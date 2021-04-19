---
description: L’utilisation de la fonctionnalité IMM dans votre application prenant en charge l’IME évite aux utilisateurs d’avoir à mémoriser toutes les valeurs de caractères possibles.
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: À propos du gestionnaire de méthode d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522080"
---
# <a name="about-input-method-manager"></a><span data-ttu-id="12457-103">À propos du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="12457-103">About Input Method Manager</span></span>

<span data-ttu-id="12457-104">L’utilisation de la fonctionnalité IMM dans votre application prenant en charge l’IME évite aux utilisateurs d’avoir à mémoriser toutes les valeurs de caractères possibles.</span><span class="sxs-lookup"><span data-stu-id="12457-104">Use of the IMM functionality in your IME-aware application relieves users of the need to remember all possible character values.</span></span> <span data-ttu-id="12457-105">Au lieu de cela, il permet à l’IME de surveiller les séquences de touches d’un utilisateur, anticipe les caractères que l’utilisateur peut souhaiter, et présente une liste de caractères candidats à choisir.</span><span class="sxs-lookup"><span data-stu-id="12457-105">Instead, it allows the IME to monitor a user's keystrokes, anticipates the characters the user might want, and presents a list of candidate characters from which to choose.</span></span>

> [!Note]  
> <span data-ttu-id="12457-106">Le IMM effectue des opérations similaires à celles de l' [infrastructure de services de texte](../tsf/text-services-framework.md), utilisée par les applications qui communiquent avec les services de texte.</span><span class="sxs-lookup"><span data-stu-id="12457-106">The IMM performs similar operations to those of the [Text Services Framework](../tsf/text-services-framework.md), used by applications that communicate with text services.</span></span>

 

<span data-ttu-id="12457-107">Par défaut, le IMM fournit une fenêtre IME par le biais de laquelle l’utilisateur entre des séquences de touches et des vues et sélectionne des candidats.</span><span class="sxs-lookup"><span data-stu-id="12457-107">By default, the IMM provides an IME window through which the user enters keystrokes and views and selects candidates.</span></span> <span data-ttu-id="12457-108">Les applications peuvent utiliser les fonctions et les messages IMM pour créer et gérer leurs propres fenêtres IME, en fournissant une interface personnalisée tout en utilisant les fonctionnalités de conversion de l’IME.</span><span class="sxs-lookup"><span data-stu-id="12457-108">Applications can use the IMM functions and messages to create and manage their own IME windows, providing a custom interface while using the conversion capabilities of the IME.</span></span>

<span data-ttu-id="12457-109">Le IMM est activé uniquement sur les systèmes d’exploitation Windows localisés pour l’Asie de l’est (chinois, japonais, coréen).</span><span class="sxs-lookup"><span data-stu-id="12457-109">The IMM is only enabled on East Asian (Chinese, Japanese, Korean) localized Windows operating systems.</span></span> <span data-ttu-id="12457-110">Sur ces systèmes, l’application appelle [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) avec le \_ DBCSENABLED SM pour déterminer si le IMM est activé.</span><span class="sxs-lookup"><span data-stu-id="12457-110">On these systems, the application calls [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_DBCSENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="12457-111">**Windows 2000 :** La prise en charge complète des IMM est fournie dans toutes les versions localisées de la langue.</span><span class="sxs-lookup"><span data-stu-id="12457-111">**Windows 2000:** Full-featured IMM support is provided in all localized language versions.</span></span> <span data-ttu-id="12457-112">Toutefois, le IMM est activé uniquement lorsqu’un module linguistique asiatique est installé.</span><span class="sxs-lookup"><span data-stu-id="12457-112">However, the IMM is enabled only when an Asian language pack is installed.</span></span> <span data-ttu-id="12457-113">Une application compatible avec l’IME peut appeler [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) avec SM \_ IMMENABLED pour déterminer si le IMM est activé.</span><span class="sxs-lookup"><span data-stu-id="12457-113">An IME-aware application can call [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_IMMENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="12457-114">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="12457-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="12457-115">Listes de candidats</span><span class="sxs-lookup"><span data-stu-id="12457-115">Candidate Lists</span></span>](candidate-lists.md)
-   [<span data-ttu-id="12457-116">Chaîne de composition</span><span class="sxs-lookup"><span data-stu-id="12457-116">Composition String</span></span>](composition-string.md)
-   [<span data-ttu-id="12457-117">IME HexToUnicode</span><span class="sxs-lookup"><span data-stu-id="12457-117">HexToUnicode IME</span></span>](hextounicode-ime.md)
-   [<span data-ttu-id="12457-118">Touches d’accès rapide</span><span class="sxs-lookup"><span data-stu-id="12457-118">Hot Keys</span></span>](hot-keys.md)
-   [<span data-ttu-id="12457-119">Messages IME</span><span class="sxs-lookup"><span data-stu-id="12457-119">IME Messages</span></span>](ime-messages.md)
-   [<span data-ttu-id="12457-120">Classe de fenêtre IME</span><span class="sxs-lookup"><span data-stu-id="12457-120">IME Window Class</span></span>](ime-window-class.md)
-   [<span data-ttu-id="12457-121">Contexte d’entrée</span><span class="sxs-lookup"><span data-stu-id="12457-121">Input Context</span></span>](input-context.md)
-   [<span data-ttu-id="12457-122">Fenêtres État, composition et candidats</span><span class="sxs-lookup"><span data-stu-id="12457-122">Status, Composition, and Candidates Windows</span></span>](status--composition--and-candidates-windows.md)

 

 
