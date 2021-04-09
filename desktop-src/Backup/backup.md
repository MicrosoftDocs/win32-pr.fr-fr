---
title: Sauvegarde
description: Autoriser les applications de sauvegarde à communiquer avec d’autres applications et services sur les opérations de sauvegarde et de restauration. Effectuez une sauvegarde sur bande, initialisez une bande et récupérez les informations de lecteur de bande. Conserver les fichiers dupliqués avec SIS (Single-Instance Store).
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- sauvegarde de sauvegarde
- sauvegarde de sauvegarde, page d’hébergement
- Sauvegarde des opérations de restauration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689a5a4613bdf029b270947b523727ea00a6e05d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101996"
---
# <a name="backup"></a>Sauvegarde

Les clés de Registre pour la sauvegarde et la restauration permettent aux applications de sauvegarde de communiquer avec d’autres applications et services sur les opérations de sauvegarde et de restauration. Pour plus d’informations, consultez [clés et valeurs de Registre pour la sauvegarde et la restauration](registry-keys-for-backup-and-restore.md).

L’API de sauvegarde sur bande permet aux applications de sauvegarde de lire et d’écrire sur une bande, d’initialiser une bande et de récupérer les informations sur les lecteurs de bande ou de bande. Pour plus d’informations, consultez [sauvegarde sur bande](tape-backup.md).

SIS (Single-Instance Store) est une architecture conçue pour gérer les fichiers dupliqués avec un minimum de surcharge. L’application de sauvegarde utilise l’API de sauvegarde SIS pour accéder à l’architecture SIS. Pour plus d’informations, consultez [stockage d’instance unique et sauvegarde SIS](single-instance-store-and-sis-backup.md).

La sauvegarde et la restauration de fichiers chiffrés sont activées par l’API de chiffrement brut, qui lit et écrit les fichiers chiffrés tout en conservant les données au format chiffré. L’API permet de sauvegarder et de restaurer les données chiffrées dans ces fichiers, tout en respectant les objectifs de maintien de la sécurité des données sauvegardées et de les utiliser par une application qui n’a pas l’autorisation d’utiliser les clés de chiffrement sur le fichier. Pour plus d’informations, consultez [sauvegarde et restauration de fichiers chiffrés](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).

L’outil srdelayed peut permettre aux applications de récupération de l’état du système de déplacer, supprimer et définir le nom abrégé des fichiers système. Pour plus d’informations, consultez [Srdelayed.exe](srdelayed-exe.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de sauvegarde](backup-reference.md)
</dt> </dl>

 

 