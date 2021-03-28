---
title: Informations sur le pilote de périphérique
description: Les pilotes de périphérique et les modules sont similaires en ce sens qu’ils sont tous deux basés sur des fichiers PE.
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0735e791b8c6e1fc7434decc7ac71ccb5c1c469e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028834"
---
# <a name="device-driver-information"></a>Informations sur le pilote de périphérique

Les pilotes de périphérique et les modules sont similaires en ce sens qu’ils sont tous deux basés sur des fichiers PE. Toutefois, bien que chaque processus possède sa propre liste privée de modules chargés, les pilotes de périphérique ont des modules qui sont globaux pour le système. Par conséquent, PSAPI possède des fonctions spécifiques pour obtenir la liste des pilotes de périphériques et leurs noms.

Vous pouvez récupérer l’adresse de chargement de chaque pilote de périphérique en appelant la fonction [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) . Cette fonction remplit un tableau de valeurs **LPVOID** avec les adresses de chargement de tous les pilotes de périphérique dans le système.

La fonction [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) prend une adresse de chargement de pilote comme entrée et remplit une mémoire tampon avec le nom de base du pilote (par exemple, Win32k.sys). Une fonction associée, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), accepte les mêmes paramètres et retourne le chemin d’accès au pilote de périphérique (par exemple, C : \\ Windows \\ system32 \\Win32k.sys).

 

 




