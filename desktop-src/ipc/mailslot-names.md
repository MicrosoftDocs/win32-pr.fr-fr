---
description: Nommer des mailslots et placer des messages dans les mailslots.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Noms des mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749685"
---
# <a name="mailslot-names"></a><span data-ttu-id="8fee3-103">Noms des mailslot</span><span class="sxs-lookup"><span data-stu-id="8fee3-103">Mailslot Names</span></span>

<span data-ttu-id="8fee3-104">Quand un processus crée un mailslot, le nom du mailslot doit se présenter sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="8fee3-104">When a process creates a mailslot, the mailslot name must have the following form.</span></span>

<span data-ttu-id="8fee3-105">\\\\.\\ nom du \\ \[ *chemin d’accès* mailslot \\ \] </span><span class="sxs-lookup"><span data-stu-id="8fee3-105">\\\\.\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="8fee3-106">Un nom de mailslot requiert les éléments suivants : deux barres obliques inverses pour commencer le nom, un point, une barre oblique inverse après le point, le mot « mailslot » et une barre oblique inverse de fin.</span><span class="sxs-lookup"><span data-stu-id="8fee3-106">A mailslot name requires the following elements: two backslashes to begin the name, a period, a backslash following the period, the word "mailslot", and a trailing backslash.</span></span> <span data-ttu-id="8fee3-107">Les noms ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="8fee3-107">Names are not case sensitive.</span></span> <span data-ttu-id="8fee3-108">Un nom de mailslot peut être précédé d’un chemin d’accès composé des noms d’un ou de plusieurs répertoires, séparés par des barres obliques inverses.</span><span class="sxs-lookup"><span data-stu-id="8fee3-108">A mailslot name can be preceded by a path consisting of the names of one or more directories, separated by backslashes.</span></span> <span data-ttu-id="8fee3-109">Par exemple, si un utilisateur attend des messages sur les taxes de Bob, Pete et Sue, l’application mailslot de l’utilisateur peut autoriser l’utilisateur à créer des mailslots individuels pour chaque expéditeur, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="8fee3-109">For example, if a user expects messages on the subject of taxes from Bob, Pete, and Sue, the user's mailslot application might allow the user to create individual mailslots for each sender, as shown here:</span></span><dl> <span data-ttu-id="8fee3-110">\\\\.\\ \\ \\ Commentaires bobs les taxes sur les mailslot \_</span><span class="sxs-lookup"><span data-stu-id="8fee3-110">\\\\.\\mailslot\\taxes\\bobs\_comments</span></span>  
<span data-ttu-id="8fee3-111">\\\\.\\ \\commentaires des hypertaxations de mailslot \\ \_</span><span class="sxs-lookup"><span data-stu-id="8fee3-111">\\\\.\\mailslot\\taxes\\petes\_comments</span></span>  
<span data-ttu-id="8fee3-112">\\\\.\\ \\ \\ Commentaires écritures les taxes sur les mailslot \_</span><span class="sxs-lookup"><span data-stu-id="8fee3-112">\\\\.\\mailslot\\taxes\\sues\_comments</span></span>  
</dl>

<span data-ttu-id="8fee3-113">Pour placer un message dans un mailslot, un processus ouvre un mailslot par son nom.</span><span class="sxs-lookup"><span data-stu-id="8fee3-113">To put a message into a mailslot, a process opens a mailslot by name.</span></span> <span data-ttu-id="8fee3-114">Pour écrire sur un serveur mailslot sur l’ordinateur local, un processus peut utiliser un nom de mailslot qui a la même forme que celle utilisée pour créer un mailslot.</span><span class="sxs-lookup"><span data-stu-id="8fee3-114">To write to a mailslot on the local computer, a process can use a mailslot name that has the same form used for creating a mailslot.</span></span> <span data-ttu-id="8fee3-115">Toutefois, cette situation est relativement rare.</span><span class="sxs-lookup"><span data-stu-id="8fee3-115">This situation, however, is relatively uncommon.</span></span> <span data-ttu-id="8fee3-116">Plus souvent, vous utiliserez le formulaire suivant pour écrire sur un serveur mailslot sur un ordinateur distant spécifique :</span><span class="sxs-lookup"><span data-stu-id="8fee3-116">More frequently, you would use the following form to write to a mailslot on a specific remote computer:</span></span>

<span data-ttu-id="8fee3-117">\\\\*Nom de l’ordinateur* \\ nom du \\ \[ *chemin d’accès* mailslot \\ \] </span><span class="sxs-lookup"><span data-stu-id="8fee3-117">\\\\*ComputerName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="8fee3-118">Pour placer un message dans chaque mailslot dans le domaine spécifié avec un nom donné, utilisez la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="8fee3-118">To put a message into every mailslot in the specified domain with a given name, use the following form:</span></span>

<span data-ttu-id="8fee3-119">\\\\*Nom_domaine* \\ nom du \\ \[ *chemin d’accès* mailslot \\ \] </span><span class="sxs-lookup"><span data-stu-id="8fee3-119">\\\\*DomainName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="8fee3-120">Pour placer un message dans chaque mailslot portant un nom donné dans le domaine principal du système, utilisez la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="8fee3-120">To put a message into every mailslot with a given name in the system's primary domain, use the following form:</span></span>

<span data-ttu-id="8fee3-121">\\\\\*\\nom du \\ \[ *chemin d’accès* mailslot \\ \] </span><span class="sxs-lookup"><span data-stu-id="8fee3-121">\\\\\*\\mailslot\\\[*path*\\\]*name*</span></span>

 

 



