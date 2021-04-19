---
description: Schannel possède un ensemble bien défini de comportements pour les informations incomplètes ou excédentaires incluses dans les mémoires tampons d’entrée de ces fonctions.
ms.assetid: 5fad1e76-6520-4ff7-b2b0-2cc2061062a1
title: Mémoires tampons supplémentaires retournées par Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c9ce7a468b1b04389ad19f91785b64fb50e74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545850"
---
# <a name="extra-buffers-returned-by-schannel"></a>Mémoires tampons supplémentaires retournées par Schannel

Les informations doivent être envoyées entre le client et le serveur lors de l’établissement d’un [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) et par la suite, car les messages sécurisés sont échangés à l’aide des fonctionnalités de chiffrement et de déchiffrement fournies par Schannel. Les fonctions suivantes sont utilisées pour accomplir ces tâches :

-   [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
-   [**InitializeSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
-   [**DecryptMessage (général)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)

Schannel possède un ensemble bien défini de comportements pour les informations incomplètes ou excédentaires incluses dans les mémoires tampons d’entrée de ces fonctions. Les informations sont échangées entre le client et le serveur de la manière suivante :

1.  Le tiers local interagit avec Schannel en appelant une fonction SSPI et en transmettant les informations. En règle générale, les informations ont été reçues du tiers distant.
2.  La fonction retourne un code d’État et des mémoires tampons de sortie contenant des informations.
3.  En fonction du code d’État, les mémoires tampons de sortie sont envoyées au tiers distant au moyen d’un mécanisme de communication.
4.  Le tiers distant lit les informations envoyées par le tiers local.
5.  La boucle se répète, avec les parties locales et distantes interchangeables. (Le tiers distant appelle une fonction SSPI et transmet les informations lues à l’étape précédente.)

Tout fonctionne comme prévu lorsque la mémoire tampon d’entrée de la fonction SSPI contient exactement les informations nécessaires. Toutefois, en raison de la nature orientée flux de certains protocoles de communication, ce n’est peut-être pas le cas. un bloc d’informations reçues d’un tiers distant peut contenir moins de données que le nombre requis ou plus de données qu’il n’est possible de traiter par Schannel dans un appel de fonction unique.

Si la mémoire tampon d’entrée contient trop peu d’informations, le message Functions Return s \_ E \_ incomplet \_ . L’appelant doit obtenir des données supplémentaires du tiers distant et appeler à nouveau la fonction.

Lorsque les mémoires tampons d’entrée contiennent trop d’informations, Schannel ne traite pas ce problème comme une erreur. La fonction traite autant de l’entrée que possible, et retourne le code d’État pour cette activité de traitement. En outre, Schannel indique la présence d’informations non traitées dans les tampons d’entrée en retournant une mémoire tampon de sortie de type SECBUFFER \_ extra. Le test des tampons de sortie pour ce type de mémoire tampon est le seul moyen de détecter cette situation. Le champ **cbBuffer** de la structure de mémoire tampon supplémentaire indique le nombre d’octets d’entrée qui n’ont pas été traités.

> [!Note]  
> Le champ **pvBuffer** de la mémoire tampon supplémentaire ne contient pas de copie des données excédentaires.

 

Si vous recevez une mémoire tampon supplémentaire à partir d’une fonction SSPI, vous devez supprimer les informations déjà traitées de la mémoire tampon d’entrée et appeler à nouveau la fonction. Schannel peut et, souvent, retourne uniquement la mémoire tampon supplémentaire et rien d’autre dans les tampons de sortie.

 

 
