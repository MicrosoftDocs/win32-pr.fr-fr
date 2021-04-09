---
description: Avec un contexte orienté connexion, l’appelant de la fonction est responsable de la mise en forme des messages. L’appelant s’appuie sur le package de sécurité pour authentifier les connexions et pour garantir l’intégrité des parties spécifiques du message.
ms.assetid: 82c6b1aa-304c-47f9-8e0f-ad70a89772aa
title: Contextes de Connection-Oriented
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb9430cbcfd0536d18cd5cbd965c9f4a71742eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114938"
---
# <a name="connection-oriented-contexts"></a><span data-ttu-id="a1f77-104">Contextes de Connection-Oriented</span><span class="sxs-lookup"><span data-stu-id="a1f77-104">Connection-Oriented Contexts</span></span>

<span data-ttu-id="a1f77-105">Avec un [*contexte*](/windows/desktop/SecGloss/c-gly)orienté connexion, l’appelant de la fonction est responsable de la mise en forme des messages.</span><span class="sxs-lookup"><span data-stu-id="a1f77-105">With a connection-oriented [*context*](/windows/desktop/SecGloss/c-gly), the function's caller is responsible for formatting messages.</span></span> <span data-ttu-id="a1f77-106">L’appelant s’appuie sur le [*package de sécurité*](/windows/desktop/SecGloss/s-gly) pour authentifier les connexions et pour garantir l’intégrité des parties spécifiques du message.</span><span class="sxs-lookup"><span data-stu-id="a1f77-106">The caller relies on the [*security package*](/windows/desktop/SecGloss/s-gly) to authenticate connections and to ensure the integrity of specific parts of the message.</span></span>

<span data-ttu-id="a1f77-107">La plupart des options de contexte sont disponibles pour les contextes orientés connexion.</span><span class="sxs-lookup"><span data-stu-id="a1f77-107">Most context options are available to connection-oriented contexts.</span></span> <span data-ttu-id="a1f77-108">Ces options incluent l’authentification mutuelle, la détection de relecture et la détection de séquence, comme décrit dans [spécifications de contexte](context-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a1f77-108">These options include mutual authentication, replay detection, and sequence detection, as described in [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="a1f77-109">Un package de sécurité définit l' \_ \_ indicateur de connexion de l’indicateur SECPKG pour indiquer qu’il prend en charge la sémantique orientée connexion.</span><span class="sxs-lookup"><span data-stu-id="a1f77-109">A security package sets the SECPKG\_FLAG\_CONNECTION flag to indicate that it supports connection-oriented semantics.</span></span>

 

 
