---
title: Raccourcis et variantes de commande
description: Raccourcis et variantes de commande
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674553"
---
# <a name="command-shortcuts-and-variations"></a><span data-ttu-id="bec15-103">Raccourcis et variantes de commande</span><span class="sxs-lookup"><span data-stu-id="bec15-103">Command Shortcuts and Variations</span></span>

<span data-ttu-id="bec15-104">Vous pouvez utiliser plusieurs raccourcis quand vous utilisez des commandes MCI.</span><span class="sxs-lookup"><span data-stu-id="bec15-104">You can use several shortcuts when working with MCI commands.</span></span> <span data-ttu-id="bec15-105">Ces raccourcis vous permettent d’utiliser un identificateur unique pour faire référence à tous les appareils ouverts par votre application, ou d’ouvrir un appareil sans émettre explicitement une commande [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="bec15-105">These shortcuts enable you to use a single identifier to refer to all the devices your application has opened, or to open a device without explicitly issuing an [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="bec15-106">Vous pouvez spécifier « All » ( \_ tous les \_ \_ ID d’appareil MCI) comme identificateur d’appareil pour toute commande qui ne retourne pas d’informations.</span><span class="sxs-lookup"><span data-stu-id="bec15-106">You can specify "all" (MCI\_ALL\_DEVICE\_ID) as a device identifier for any command that does not return information.</span></span> <span data-ttu-id="bec15-107">Lorsque vous spécifiez « All », MCI envoie la commande de manière séquentielle à tous les appareils ouverts par l’application actuelle.</span><span class="sxs-lookup"><span data-stu-id="bec15-107">When you specify "all", MCI sends the command sequentially to all devices opened by the current application.</span></span>

<span data-ttu-id="bec15-108">Par exemple, la commande [**Fermer**](close.md) « tout » ferme tous les appareils ouverts et la commande [**lire**](play.md) « tout » démarre la lecture de tous les appareils ouverts par l’application.</span><span class="sxs-lookup"><span data-stu-id="bec15-108">For example, the [**close**](close.md) "all" command closes all open devices and the [**play**](play.md) "all" command starts playing all devices opened by the application.</span></span> <span data-ttu-id="bec15-109">Étant donné que le MCI envoie séquentiellement les commandes aux périphériques MCI, il existe un intervalle entre le moment où le premier et le dernier périphérique reçoit la commande.</span><span class="sxs-lookup"><span data-stu-id="bec15-109">Because MCI sequentially sends the commands to the MCI devices, there is an interval between when the first and last devices receive the command.</span></span>

<span data-ttu-id="bec15-110">L’utilisation de « All » est un moyen pratique de diffuser une commande sur tous vos appareils, mais vous ne devez pas vous en servir pour synchroniser les appareils. le délai entre les messages peut varier.</span><span class="sxs-lookup"><span data-stu-id="bec15-110">Using "all" is a convenient way to broadcast a command to all your devices, but you should not rely on it to synchronize devices; the timing between messages can vary.</span></span>

<span data-ttu-id="bec15-111">Lorsque vous émettez une commande et spécifiez un appareil qui n’est pas ouvert, MCI tente d’ouvrir l’appareil avant d’implémenter la commande.</span><span class="sxs-lookup"><span data-stu-id="bec15-111">When you issue a command and specify a device that is not open, MCI tries to open the device before implementing the command.</span></span> <span data-ttu-id="bec15-112">Les règles suivantes s’appliquent à l’ouverture automatique des appareils :</span><span class="sxs-lookup"><span data-stu-id="bec15-112">The following rules apply to automatically opening devices:</span></span>

-   <span data-ttu-id="bec15-113">La fonctionnalité d’ouverture automatique fonctionne uniquement avec l’interface de chaîne de commande.</span><span class="sxs-lookup"><span data-stu-id="bec15-113">The automatic open feature works only with the command-string interface.</span></span>
-   <span data-ttu-id="bec15-114">La fonctionnalité d’ouverture automatique échoue pour les commandes qui sont spécifiques aux pilotes de périphérique personnalisés.</span><span class="sxs-lookup"><span data-stu-id="bec15-114">The automatic open feature fails for commands that are specific to custom device drivers.</span></span>
-   <span data-ttu-id="bec15-115">Les appareils ouverts automatiquement ne répondent pas aux commandes qui utilisent « All » comme nom de périphérique.</span><span class="sxs-lookup"><span data-stu-id="bec15-115">Automatically opened devices do not respond to commands that use "all" as a device name.</span></span>
-   <span data-ttu-id="bec15-116">La fonctionnalité d’ouverture automatique ne permet pas à votre application de spécifier l’indicateur « type ».</span><span class="sxs-lookup"><span data-stu-id="bec15-116">The automatic open feature does not let your application specify the "type" flag.</span></span> <span data-ttu-id="bec15-117">Sans le nom de l’appareil, MCI détermine le nom de l’appareil à partir des entrées du Registre.</span><span class="sxs-lookup"><span data-stu-id="bec15-117">Without the device name, MCI determines the device name from the entries in the registry.</span></span> <span data-ttu-id="bec15-118">Pour utiliser un appareil spécifique, vous pouvez combiner le nom de l’appareil avec le nom de fichier à l’aide du point d’exclamation, comme décrit dans la documentation de référence pour la commande [**ouvrir**](open.md) .</span><span class="sxs-lookup"><span data-stu-id="bec15-118">To use a specific device, you can combine the device name with the filename by using the exclamation point, as described in the reference material for the [**open**](open.md) command.</span></span>

<span data-ttu-id="bec15-119">Si une application utilise la fonctionnalité d’ouverture automatique pour ouvrir un appareil, l’application doit vérifier la valeur de retour de chaque commande Open suivante pour vérifier que l’appareil est toujours ouvert.</span><span class="sxs-lookup"><span data-stu-id="bec15-119">If an application uses the automatic open feature to open a device, the application should check the return value of every subsequent open command to verify that the device is still open.</span></span> <span data-ttu-id="bec15-120">MCI ferme également automatiquement tous les appareils qu’il ouvre automatiquement.</span><span class="sxs-lookup"><span data-stu-id="bec15-120">MCI also automatically closes any device that it automatically opens.</span></span> <span data-ttu-id="bec15-121">MCI ferme généralement un appareil dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="bec15-121">MCI typically closes a device in the following situations:</span></span>

-   <span data-ttu-id="bec15-122">La commande est terminée.</span><span class="sxs-lookup"><span data-stu-id="bec15-122">The command is completed.</span></span>
-   <span data-ttu-id="bec15-123">Vous abandonnez la commande.</span><span class="sxs-lookup"><span data-stu-id="bec15-123">You abort the command.</span></span>
-   <span data-ttu-id="bec15-124">Vous demandez une notification dans une commande ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bec15-124">You request notification in a subsequent command.</span></span>
-   <span data-ttu-id="bec15-125">MCI détecte une défaillance.</span><span class="sxs-lookup"><span data-stu-id="bec15-125">MCI detects a failure.</span></span>

 

 




