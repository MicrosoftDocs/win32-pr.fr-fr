---
description: Pour qu’une application puisse utiliser l’une des fonctions de téléphone supplémentaires TAPIs 30, elle a besoin d’une connexion à TAPI, par l’intermédiaire de laquelle elle peut recevoir des messages.
ms.assetid: c0211f64-4f73-4348-ae49-9a898d3aa093
title: Initialisation et arrêt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6831b8cfda84ac564450caec554191198fd4c21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518977"
---
# <a name="initialization-and-shutdown"></a>Initialisation et arrêt

Pour qu’une application puisse utiliser les 30 fonctions de téléphone supplémentaires de TAPI, elle a besoin d’une connexion à l’interface TAPI, par l’intermédiaire de laquelle elle peut recevoir des messages. L’application établit cette connexion à l’aide de la fonction [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) . Dans cette fonction, l’application spécifie le mécanisme de notification par lequel TAPI informe l’application des modifications de l’état du téléphone et de l’achèvement asynchrone des fonctions de téléphone.

La fonction [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) retourne deux informations à l’application : un handle d' *application* et le nombre d’appareils téléphoniques. Le descripteur d’application représente l’utilisation de l’application TAPI. Les fonctions TAPI qui utilisent des handles téléphoniques n’ont pas besoin du descripteur d’application, car ce descripteur est dérivé du descripteur téléphonique spécifié.

La deuxième information retournée par [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) est le nombre d’appareils téléphoniques disponibles pour l’interface TAPI. Les appareils téléphoniques sont identifiés par leur identificateur d’appareil (*ID d’appareil*). Les identificateurs d’appareil valides sont compris entre zéro et le nombre d’appareils téléphoniques moins un. Par exemple, si **phoneInitializeEx** signale qu’il y a deux appareils téléphoniques dans un système, les identificateurs de périphérique téléphonique valides sont 0 et 1. Une fois qu’une application a fini d’utiliser les fonctions de téléphonie de TAPI, elle appelle [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown), en transmettant son handle d’application pour arrêter son utilisation de l’interface TAPI. Cela permet à TAPI de libérer toutes les ressources affectées à l’application.

Les applications ne doivent pas appeler [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) sans ouvrir par la suite un téléphone (au moins pour la surveillance). Si l’application n’analyse pas et n’utilise pas d’appareils, elle doit appeler [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) afin que les ressources de mémoire allouées par la bibliothèque de liens dynamiques TAPI puissent être libérées si elles ne sont pas nécessaires, et la bibliothèque elle-même peut être déchargée de la mémoire alors qu’elle n’est pas nécessaire.

[**PhoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) et [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) fonctionnent de manière synchrone. Autrement dit, ces fonctions retournent une indication de réussite ou d’échec et ne retournent jamais d’identificateur de demande asynchrone.

 

 



