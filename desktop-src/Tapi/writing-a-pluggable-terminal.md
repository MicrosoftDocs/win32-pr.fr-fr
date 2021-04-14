---
description: Normalement, un fournisseur de services de média (MSP) implémente la création de terminal.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Écriture d’un terminal enfichable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cbfe2da0c121fcee820d47fd57216840d23c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526811"
---
# <a name="writing-a-pluggable-terminal"></a><span data-ttu-id="99f01-103">Écriture d’un terminal enfichable</span><span class="sxs-lookup"><span data-stu-id="99f01-103">Writing a Pluggable Terminal</span></span>

<span data-ttu-id="99f01-104">Normalement, un fournisseur de services de média (MSP) implémente la création de terminal.</span><span class="sxs-lookup"><span data-stu-id="99f01-104">Normally, a media service provider (MSP) implements terminal creation.</span></span> <span data-ttu-id="99f01-105">À compter de Windows 2000 SP1, TAPI 3 comprend des terminaux enfichables pour permettre à une application d’implémenter la création de terminal.</span><span class="sxs-lookup"><span data-stu-id="99f01-105">Starting with Windows 2000 SP1, TAPI 3 includes pluggable terminals to allow an application to implement terminal creation.</span></span> <span data-ttu-id="99f01-106">Pour plus d’informations sur l’utilisation de ces terminaux, consultez la vue d’ensemble de l' [implémentation de terminaux enfichables](implementing-pluggable-terminals.md) .</span><span class="sxs-lookup"><span data-stu-id="99f01-106">Please see the overview on [implementing pluggable terminals](implementing-pluggable-terminals.md) for additional information on using these terminals.</span></span>

<span data-ttu-id="99f01-107">Vous ne devez pas utiliser les terminaux enfichables régulièrement, car les fonctionnalités complètes d’un terminal ne sont disponibles que lorsqu’un MSP en est pleinement conscient.</span><span class="sxs-lookup"><span data-stu-id="99f01-107">You should not use pluggable terminals routinely because the full capabilities of a terminal will only be available when an MSP is fully aware of it.</span></span> <span data-ttu-id="99f01-108">En outre, vous ne devez pas tenter d’implémenter des terminaux enfichables, sauf si vous êtes déjà familiarisé avec l’écriture de fournisseurs de services multimédias.</span><span class="sxs-lookup"><span data-stu-id="99f01-108">Further, you should not attempt to implement pluggable terminals unless you are already familiar with writing media service providers.</span></span> <span data-ttu-id="99f01-109">Les techniques et problèmes potentiels impliqués sont très similaires.</span><span class="sxs-lookup"><span data-stu-id="99f01-109">The techniques and potential problems involved are quite similar.</span></span>

<span data-ttu-id="99f01-110">La mise en service d’un cas particulier de terminal enfichable existe actuellement pour la situation d’un serveur de conférence qui doit ajouter des clients non-Windows 2000 SP1 ou non multicast H. 323 à des conférences de multidiffusion SDP/IP multiparts TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="99f01-110">Provision for a special case of pluggable terminal currently exists for the situation of a conferencing server that needs to add non-Windows 2000 SP1 or nonmulticast H.323 clients to TAPI 3 multiparty SDP/IP multicast conferences.</span></span>

 

 



