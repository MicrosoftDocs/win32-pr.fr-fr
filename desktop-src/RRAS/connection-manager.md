---
title: Gestionnaire de connexions
description: Les clients qui envisagent de développer des numéroteurs personnalisés à l’aide de l’API du service d’accès à distance peuvent souhaiter enquêter sur le gestionnaire de connexions Microsoft et le kit d’administration du gestionnaire des connexions.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104030868"
---
# <a name="connection-manager"></a>Gestionnaire de connexions

Les clients qui envisagent de développer des numéroteurs personnalisés à l’aide de l’API du service d’accès à distance peuvent souhaiter enquêter sur le gestionnaire de connexions Microsoft et le kit d’administration du gestionnaire des connexions. Le gestionnaire de connexions est le client d’accès à distance géré de Microsoft. Il permet à un administrateur de créer un package de configuration d’accès à distance à distribuer aux utilisateurs distants de l’administrateur. Pour plus d’informations sur le gestionnaire de connexions et le kit d’administration du gestionnaire des connexions, consultez l’aide en ligne pour Microsoft Windows 2000 Server et les systèmes d’exploitation ultérieurs.

Vous pouvez trouver le code source d’un exemple d’action personnalisée du gestionnaire de connexions dans le kit de développement logiciel (SDK) complet de la plateforme. Le kit de développement logiciel (SDK) de plateforme peut être téléchargé sur le [site Web de Microsoft](https://msdn.microsoft.com/windowsserver/bb980924.aspx). Après l’installation, le chemin d’accès à l’exemple de code est% install chemin% \\ Microsoft SDK \\ Samples \\ netds \\ RAS \\ ConnectionManager, où% install Path% désigne le répertoire d’installation de base du kit de développement logiciel (SDK) de la plateforme (par exemple, C : \\ Program Files).

Les actions personnalisées permettent au client d’accès à distance d’effectuer des actions spécifiques à différents stades du processus de connexion. L’action personnalisée présentée dans l’exemple ajuste automatiquement la configuration du serveur proxy pour une connexion en fonction de l’adresse du serveur de la connexion. Les clients peuvent utiliser cet exemple comme point de départ pour créer leurs propres actions personnalisées.

 

 




