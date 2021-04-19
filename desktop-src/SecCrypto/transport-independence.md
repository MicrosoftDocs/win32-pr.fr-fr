---
description: Les certificats peuvent être demandés et distribués via n’importe quel mécanisme de transport.
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: Indépendance du transport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8d68b8f6312495c242f6b2bd2ea75301f802c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521434"
---
# <a name="transport-independence"></a>Indépendance du transport

Les certificats peuvent être demandés et distribués via n’importe quel mécanisme de transport. Les services de certificats acceptent les [*demandes de certificat*](../secgloss/c-gly.md) d’un demandeur via http, DCOM, RPC, un fichier disque ou un transport personnalisé. Les services de certificats publient des certificats au demandeur via HTTP, DCOM, RPC, un fichier de disque ou un transport personnalisé.

Les transports sont pris en charge par les applications intermédiaires et les dll du module de sortie, généralement écrites en C/C++. Les applications intermédiaires et les modules de sortie isolent les fonctions des services de certificats de la communication avec un transport spécifique.

 

 
