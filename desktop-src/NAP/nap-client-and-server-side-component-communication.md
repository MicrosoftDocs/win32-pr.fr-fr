---
title: Communication entre le client NAP et le composant côté serveur
description: Communication entre le client NAP et le composant côté serveur
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110606"
---
# <a name="nap-client-and-server-side-component-communication"></a>Communication entre le client NAP et le composant côté serveur

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

Le composant agent NAP peut communiquer avec le composant serveur d’administration NAP par le biais du processus suivant :

1.  L’agent NAP transmet le SSoH à la EC NAP.
2.  La EC NAP transmet le SSoH aux NAP.
3.  La protection NAP des e/s transmet le SSoH au service NPS (Network Policy Server).
4.  Le service NPS transmet le SSoH au serveur d’administration NAP.

Un agent SHA peut communiquer avec son validateur d’intégrité de l’un des processus suivants :

1.  L’algorithme SHA passe son SoH à l’agent NAP.
2.  L’agent NAP passe l’SoH contenue dans SSoH à la EC NAP.
3.  La EC NAP passe l’SoH aux NAP.
4.  La protection d’accès réseau (NAP) transmet la déclaration d’intégrité au serveur d’administration NAP.
5.  Le serveur d’administration NAP transmet la SoH à l’SHV.

La figure ci-dessous illustre le processus de communication entre les composants clients NAP et les composants côté serveur NAP.

![architecture de communication entre le client et le serveur dans la plateforme NAP](images/nap-client-to-server-comm.png)

Le serveur d’administration NAP peut communiquer avec l’agent NAP par le biais du processus suivant :

1.  Le serveur d’administration NAP transmet le SoHRs au service NPS.
2.  Le service NPS transmet le SSoHR aux NAP.
3.  La protection NAP des e/s transmet le SSoHR à la EC NAP.
4.  La EC NAP transmet le SSoHR à l’agent NAP.

Le SHV peut communiquer avec son SHA correspondant par le biais du processus suivant :

1.  Le SHV transmet son SoHR au serveur d’administration NAP.
2.  Le serveur d’administration NAP transmet le SoHR au service NPS.
3.  Le service NPS transmet le SoHR, contenu dans le SSoHR, aux NAP ES.
4.  La protection NAP des e/s transmet le SoHR à la EC NAP.
5.  La EC NAP transmet le SoHR à l’agent NAP.
6.  L’agent NAP transmet le SoHR à l’agent SHA.

La figure ci-dessous illustre le processus de communication entre les composants côté serveur NAP et les composants clients NAP.

![architecture des communications de serveur à client dans la plateforme NAP](images/nap-server-to-client-comm.png)

 

 




