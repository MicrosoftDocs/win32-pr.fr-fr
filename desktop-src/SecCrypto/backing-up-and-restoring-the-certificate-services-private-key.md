---
description: Vous ne pouvez pas utiliser les fonctions de sauvegarde et de restauration de Certadm.dll pour sauvegarder les clés privées des services de certificats.
ms.assetid: 27ee8caa-8f5e-46dc-b55d-afde5471507e
title: Sauvegarde et restauration de la clé privée des services de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65b8c25e627e516d92b8dc8219db9c7933bd8d9902b1f75bea204d723edd61f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879779"
---
# <a name="backing-up-and-restoring-the-certificate-services-private-key"></a>Sauvegarde et restauration de la clé privée des services de certificats

Vous ne pouvez pas utiliser les fonctions de sauvegarde et de restauration de Certadm.dll pour sauvegarder les [*clés privées*](../secgloss/p-gly.md)des services de certificats. Les clés privées ne peuvent pas être sauvegardées par ces fonctions, car elles sont destinées à sauvegarder et à restaurer la base de données des services de certificats (et les fichiers associés), et cette base de données ne contient pas de clés privées (même pour les certificats auto-émis).

Pour sauvegarder une clé privée des services de certificats, utilisez le composant logiciel enfichable MMC Autorité de certification ou la commande certutil (avec-Backup ou-backupkey spécifié). La sauvegarde de la clé privée avec le composant logiciel enfichable MMC de l’autorité de certification ou de la commande certutil entraîne l’écriture de la clé privée dans un \# fichier PKCS 12. Même si ce \# fichier PKCS 12 est protégé par un mot de passe, il doit être considéré comme extrêmement sensible et doit être stocké de manière sécurisée ; le mot de passe du \# fichier PKCS 12 doit également être protégé contre les personnes non autorisées.

De même, les clés privées ne peuvent pas être restaurées par les fonctions de sauvegarde et de restauration des services de certificats. Une clé de sauvegarde des services de certificats contenue dans un \# fichier PKCS 12 peut être restaurée par le composant logiciel enfichable MMC de l’autorité de certification ou par la commande certutil (en spécifiant les verbes-Restore ou-restorekey); Notez que la personne effectuant l’opération de restauration doit connaître le mot de passe du \# fichier PKCS 12.

Il n’existe que deux cas dans lesquels une clé privée de services de certificats doit être sauvegardée. Le premier cas est après l’installation des services de certificats. Le deuxième cas est après toute opération de renouvellement du certificat des services de certificats.

 

 
