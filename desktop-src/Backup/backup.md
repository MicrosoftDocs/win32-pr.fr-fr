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
# <a name="backup"></a><span data-ttu-id="fc97d-108">Sauvegarde</span><span class="sxs-lookup"><span data-stu-id="fc97d-108">Backup</span></span>

<span data-ttu-id="fc97d-109">Les clés de Registre pour la sauvegarde et la restauration permettent aux applications de sauvegarde de communiquer avec d’autres applications et services sur les opérations de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="fc97d-109">Registry keys for backup and restore allow backup applications to communicate with other applications and services about backup and restore operations.</span></span> <span data-ttu-id="fc97d-110">Pour plus d’informations, consultez [clés et valeurs de Registre pour la sauvegarde et la restauration](registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="fc97d-110">For more information, see [Registry Keys and Values for Backup and Restore](registry-keys-for-backup-and-restore.md).</span></span>

<span data-ttu-id="fc97d-111">L’API de sauvegarde sur bande permet aux applications de sauvegarde de lire et d’écrire sur une bande, d’initialiser une bande et de récupérer les informations sur les lecteurs de bande ou de bande.</span><span class="sxs-lookup"><span data-stu-id="fc97d-111">The tape backup API enables backup applications to read from and write to a tape, initialize a tape, and retrieve tape or tape drive information.</span></span> <span data-ttu-id="fc97d-112">Pour plus d’informations, consultez [sauvegarde sur bande](tape-backup.md).</span><span class="sxs-lookup"><span data-stu-id="fc97d-112">For more information, see [Tape Backup](tape-backup.md).</span></span>

<span data-ttu-id="fc97d-113">SIS (Single-Instance Store) est une architecture conçue pour gérer les fichiers dupliqués avec un minimum de surcharge.</span><span class="sxs-lookup"><span data-stu-id="fc97d-113">Single-instance store (SIS) is an architecture designed to maintain duplicate files with a minimum of overhead.</span></span> <span data-ttu-id="fc97d-114">L’application de sauvegarde utilise l’API de sauvegarde SIS pour accéder à l’architecture SIS.</span><span class="sxs-lookup"><span data-stu-id="fc97d-114">Backup application use the SIS backup API to access the SIS architecture.</span></span> <span data-ttu-id="fc97d-115">Pour plus d’informations, consultez [stockage d’instance unique et sauvegarde SIS](single-instance-store-and-sis-backup.md).</span><span class="sxs-lookup"><span data-stu-id="fc97d-115">For more information, see [Single-Instance Store and SIS Backup](single-instance-store-and-sis-backup.md).</span></span>

<span data-ttu-id="fc97d-116">La sauvegarde et la restauration de fichiers chiffrés sont activées par l’API de chiffrement brut, qui lit et écrit les fichiers chiffrés tout en conservant les données au format chiffré.</span><span class="sxs-lookup"><span data-stu-id="fc97d-116">Backup and restore of encrypted files is enabled by the raw encryption API, which reads and writes encrypted files while keeping the data in encrypted format.</span></span> <span data-ttu-id="fc97d-117">L’API permet de sauvegarder et de restaurer les données chiffrées dans ces fichiers, tout en respectant les objectifs de maintien de la sécurité des données sauvegardées et de les utiliser par une application qui n’a pas l’autorisation d’utiliser les clés de chiffrement sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="fc97d-117">The API allows the encrypted data in these files to be backed up and restored, while meeting the goals of maintaining the security of the backed up data, and being usable by an application that lacks permission to use the encryption keys on the file.</span></span> <span data-ttu-id="fc97d-118">Pour plus d’informations, consultez [sauvegarde et restauration de fichiers chiffrés](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span><span class="sxs-lookup"><span data-stu-id="fc97d-118">For more information, see [Backup and Restore of Encrypted Files](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span></span>

<span data-ttu-id="fc97d-119">L’outil srdelayed peut permettre aux applications de récupération de l’état du système de déplacer, supprimer et définir le nom abrégé des fichiers système.</span><span class="sxs-lookup"><span data-stu-id="fc97d-119">The Srdelayed tool can enable system state recovery applications to move, delete, and set the short name of system files.</span></span> <span data-ttu-id="fc97d-120">Pour plus d’informations, consultez [Srdelayed.exe](srdelayed-exe.md).</span><span class="sxs-lookup"><span data-stu-id="fc97d-120">For more information, see [Srdelayed.exe](srdelayed-exe.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc97d-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc97d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc97d-122">Référence de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="fc97d-122">Backup Reference</span></span>](backup-reference.md)
</dt> </dl>

 

 