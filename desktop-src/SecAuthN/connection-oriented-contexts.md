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
# <a name="connection-oriented-contexts"></a>Contextes de Connection-Oriented

Avec un [*contexte*](/windows/desktop/SecGloss/c-gly)orienté connexion, l’appelant de la fonction est responsable de la mise en forme des messages. L’appelant s’appuie sur le [*package de sécurité*](/windows/desktop/SecGloss/s-gly) pour authentifier les connexions et pour garantir l’intégrité des parties spécifiques du message.

La plupart des options de contexte sont disponibles pour les contextes orientés connexion. Ces options incluent l’authentification mutuelle, la détection de relecture et la détection de séquence, comme décrit dans [spécifications de contexte](context-requirements.md).

Un package de sécurité définit l' \_ \_ indicateur de connexion de l’indicateur SECPKG pour indiquer qu’il prend en charge la sémantique orientée connexion.

 

 
