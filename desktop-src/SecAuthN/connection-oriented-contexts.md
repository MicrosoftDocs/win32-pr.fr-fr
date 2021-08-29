---
description: Avec un contexte orienté connexion, l’appelant de la fonction est responsable de la mise en forme des messages. L’appelant s’appuie sur le package de sécurité pour authentifier les connexions et pour garantir l’intégrité des parties spécifiques du message.
ms.assetid: 82c6b1aa-304c-47f9-8e0f-ad70a89772aa
title: Contextes de Connection-Oriented
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b889b948f41916e3e741311ea4289c4214cdc256084af7bb455265dd69a7d00a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141162"
---
# <a name="connection-oriented-contexts"></a>Contextes de Connection-Oriented

Avec un [*contexte*](/windows/desktop/SecGloss/c-gly)orienté connexion, l’appelant de la fonction est responsable de la mise en forme des messages. L’appelant s’appuie sur le [*package de sécurité*](/windows/desktop/SecGloss/s-gly) pour authentifier les connexions et pour garantir l’intégrité des parties spécifiques du message.

La plupart des options de contexte sont disponibles pour les contextes orientés connexion. Ces options incluent l’authentification mutuelle, la détection de relecture et la détection de séquence, comme décrit dans [spécifications de contexte](context-requirements.md).

Un package de sécurité définit l' \_ \_ indicateur de connexion de l’indicateur SECPKG pour indiquer qu’il prend en charge la sémantique orientée connexion.

 

 
