---
description: Une page de référence d’événement (ERP) est un document HTML qui fournit des informations Moniteur réseau sur les événements détectés pendant l’analyse ou l’opération de surveillance.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: À propos des pages de référence d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e989e3e1d4ab0c41dc78c567c662e8a3090906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865469"
---
# <a name="about-event-reference-pages"></a>À propos des pages de référence d’événement

Une page de référence d’événement (ERP) est un document HTML qui fournit des informations Moniteur réseau sur les événements détectés pendant l’analyse ou l’opération de surveillance.

Vous pouvez afficher vos solutions ERP dans le observateur d’événements de Moniteur réseau, l’outil de contrôle de l’analyse ou un navigateur prenant en charge les fonctionnalités HTML de Microsoft Internet Explorer version 4,01 ou ultérieure. Autrement dit, vous pouvez ajouter des contrôles pris en charge ou des langages de script dans votre ERP.

Toutefois, vos solutions ERP s’affiche uniquement si l’expert désigne le document HTML par son nom. Lorsqu’il est correctement désigné, l’ERP s’affiche dans le volet inférieur lorsque l’événement dans le observateur d’événements est sélectionné. La figure ci-dessous illustre une ERP associée à l’analyse de plage IP (Internet Protocol).

![une ERP associée à l’analyse de plage d’adresses IP](images/exview2.png)

## <a name="expert-events"></a>Événements d’experts

Les événements experts sont identifiés par le membre **EventIdent** d’une structure [**NMEVENTDATA**](nmeventdata.md) . Lorsque vous écrivez un expert, vous déterminez les valeurs de **EventIdent** , qui sont généralement numérotées 1, 2, 3, et ainsi de suite. Supposons, par exemple, qu’un expert génère deux événements (**EventIdent1** et **EventIdent2**). Si vous souhaitez que les observateur d’événements affichent les événements séparément, vous devez créer deux documents ERP distincts.

 

 



