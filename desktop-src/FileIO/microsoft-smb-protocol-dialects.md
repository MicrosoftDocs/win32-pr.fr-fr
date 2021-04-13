---
description: Pour établir une connexion entre un client et un serveur à l’aide du protocole SMB Microsoft, vous devez d’abord déterminer le dialecte avec le plus haut niveau de fonctionnalité pris en charge par le client et le serveur.
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Dialectes du protocole SMB Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484729"
---
# <a name="microsoft-smb-protocol-dialects"></a>Dialectes du protocole SMB Microsoft

La liste des paquets de messages du protocole SMB Microsoft a augmenté au fil des années pour s’adapter aux fonctionnalités croissantes du protocole SMB de Microsoft, ainsi qu’aux centaines. Chaque étape de sa croissance est marquée par un ensemble de paquets standard ou un dialecte. Chaque dialecte est identifié par une chaîne standard telle que « PC NETWORK PROGRAM 1,0 », « MICROSOFT NETWORKs 3,0 », « DOS LANMAN 2,1 » ou « NT LM 0,12 ». La première chaîne identifie le premier dialecte de SMB, et la dernière chaîne identifie CIFS, le premier dialecte du protocole SMB Microsoft.

La plupart des clients Windows prennent en charge au moins six dialectes différents du protocole SMB de Microsoft. par conséquent, l’une des premières étapes de l’établissement d’une connexion entre un client et un serveur à l’aide du protocole SMB Microsoft consiste à déterminer le dialecte avec le plus haut niveau de fonctionnalité pris en charge par le client et le serveur. Ce processus est appelé « négociation du dialecte ». Les chaînes de dialectes mentionnées ci-dessus sont incluses dans les paquets de demande et de réponse de négociation de dialecte à cet effet.

 

 



