---
description: Les objets fichier fonctionnent comme l’interface logique entre les processus du noyau et du mode utilisateur, ainsi que les données de fichier qui résident sur le disque physique.
ms.assetid: 53aabb35-4601-42d1-ac73-385473ff91e2
title: Objets fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e37793ad6c31ac86809047a3ec0d34afc3efc34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009951"
---
# <a name="file-objects"></a>Objets fichier

Les *objets fichier* fonctionnent comme l’interface logique entre les processus du noyau et du mode utilisateur, ainsi que les données de fichier qui résident sur le disque physique. Un objet file contient à la fois les données écrites dans le fichier et l’ensemble suivant d’attributs gérés par le noyau.



| Type d’informations                                              | Objectif                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom de fichier                                                     | Nomme le fichier physique correspondant.                                                                                                                                                          |
| Décalage de l’octet actuel                                           | Utilisé dans les e/s de fichier synchrones (décrit plus loin dans cette section) pour identifier l’emplacement de départ actuel des opérations de lecture et d’écriture.                                                          |
| Mode de partage                                                    | Spécifie si un deuxième processus peut ouvrir un fichier pour l’accès en lecture, en écriture ou en suppression alors que le processus initial y accède encore.                                                           |
| Mode e/s                                                      | Spécifie si le processus initial a ouvert le fichier pour des e/s [synchrones ou asynchrones](synchronous-and-asynchronous-i-o.md), des e/s mises en cache ou non, des e/s séquentielles ou aléatoires, etc. |
| Pointeur vers un objet appareil                                      | Identifie l’appareil physique sur lequel résident les données de fichier.                                                                                                                                        |
| Pointeur vers le bloc de paramètres de volume ou l’outil [ **VPB**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_vpb) | Identifie le volume ou la partition sur lequel les données de fichier résident.                                                                                                                                    |
| Pointeur vers pointeurs d’objet de section                            | Identifie une structure racine qui décrit un [fichier mappé](/windows/desktop/Memory/file-mapping).                                                                                                                  |
| Pointeur vers mappage de cache privé                                  | Identifie les données de fichier qui sont actuellement mises en cache.                                                                                                                                              |



 

Ces attributs sont définis dans le cadre de la structure de l' [**\_ objet fichier**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) dans Ntddk. h. reportez-vous à la définition de cette structure dans la documentation de Windows Driver Kit (WDK) pour les longueurs de données et les types de valeurs.

 

 
