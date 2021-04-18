---
description: À mesure que des fichiers, des répertoires et d’autres objets de système de fichiers NTFS sont ajoutés, supprimés et modifiés, le système de fichiers NTFS entre les enregistrements de journal de modification dans les flux, un pour chaque volume de l’ordinateur.
ms.assetid: c41aa3a8-c8d8-4bf2-9bbb-d6a6a556c5e4
title: Modifier les enregistrements de journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56580a28c01ca164af4598cb290a37c8e36828f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519532"
---
# <a name="change-journal-records"></a>Modifier les enregistrements de journal

À mesure que des fichiers, des répertoires et d’autres objets de système de fichiers NTFS sont ajoutés, supprimés et modifiés, le système de fichiers NTFS entre les enregistrements de journal de modification dans les flux, un pour chaque volume de l’ordinateur. Chaque enregistrement indique le type de modification et l'objet modifié. Le décalage à partir du début du flux pour un enregistrement particulier est appelé numéro de séquence de mise à jour (USN) pour l’enregistrement particulier. Les nouveaux enregistrements sont ajoutés à la fin du flux.

Le système de fichiers NTFS peut supprimer les anciens enregistrements pour conserver de l’espace. Si des enregistrements nécessaires ont été supprimés, le service d’indexation récupère en réindexant le volume, comme c’est le cas lorsqu’il n’existe pas de journal des modifications.

Le journal des modifications enregistre uniquement le fait d’une modification apportée à un fichier et la raison de la modification (par exemple, opérations d’écriture, troncation, augmentation, suppression, etc.). Il n’enregistre pas suffisamment d’informations pour permettre l’inversion de la modification.

En outre, plusieurs modifications apportées au même fichier peuvent entraîner l’ajout d’un seul indicateur de raison à l’enregistrement actuel. Si le même type de modification se produit plusieurs fois, le système de fichiers NTFS n’écrit pas un nouvel enregistrement pour les modifications après le premier. Par exemple, plusieurs opérations d’écriture sans intervention de fermeture et de réouverture n’aboutissent qu’à un seul enregistrement de modification avec la raison de l’indicateur USN raison du remplacement des données par le \_ \_ jeu de données \_ .

Pour illustrer le fonctionnement du journal des modifications, supposez qu’un utilisateur accède à un fichier dans l’ordre suivant :

1.  Écrit dans le fichier.
2.  Définit l’horodatage du fichier.
3.  Écrit dans le fichier.
4.  Tronque le fichier.
5.  Écrit dans le fichier.
6.  Ferme le fichier.

Dans ce cas, le système de fichiers NTFS effectue les actions suivantes dans le journal des modifications (où \| indique une opération or au niveau du bit).



| Événement                                 | Action du système de fichiers NTFS                                                                                                                                                                                                                                                    |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opération d’écriture initiale<br/>    | Le système de fichiers NTFS écrit un nouvel enregistrement USN avec l' \_ indicateur de raison du remplacement des données du motif USN \_ \_ défini. Pour plus d’informations sur les indicateurs de raison possibles, consultez la structure de l' [**\_ enregistrement USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) .<br/>                                                     |
| Définition de l’horodatage de fichier<br/> | Le système de fichiers NTFS écrit un nouvel enregistrement USN avec l’indicateur paramètre USN \_ motif de \_ remplacement des données USN raison de la modification des \_ \| informations de \_ \_ base \_ \_ .<br/>                                                                                                                            |
| Deuxième opération d’écriture<br/>     | Le système de fichiers NTFS n’écrit pas un nouvel enregistrement USN. Étant donné que le \_ \_ \_ remplacement des données du motif USN est déjà défini pour l’enregistrement existant, aucune modification n’est apportée à l’enregistrement.<br/>                                                                                           |
| Troncation de fichier<br/>            | Le système de fichiers NTFS écrit un nouvel enregistrement USN avec l’indicateur paramètre USN \_ motif du remplacement des données USN motif de la modification de l' \_ \_ \| \_ USN raison de la \_ \_ \_ \| \_ \_ \_ troncation des données.<br/>                                                                                           |
| Troisième opération d’écriture<br/>      | Le système de fichiers NTFS n’écrit pas un nouvel enregistrement USN. Étant donné que le \_ \_ \_ remplacement des données du motif USN est déjà défini pour l’enregistrement existant, aucune modification n’est apportée à l’enregistrement.<br/>                                                                                           |
| Opération de fermeture<br/>            | Si l’utilisateur qui apporte des modifications est le seul utilisateur du fichier, le système de fichiers NTFS écrit un nouvel enregistrement USN avec le paramètre d’indicateur suivant : valeur USN \_ motif de \_ remplacement des données \_ USN motif de modification de l' \| USN motif de la troncation des \_ données \_ \_ \_ \| \_ \_ \_ \| \_ \_ USN raison de la fermeture.<br/> |



 

Le journal des modifications accumule une série d’enregistrements entre la première ouverture et la dernière fermeture d’un fichier. Un nouvel indicateur de motif est défini pour chaque enregistrement, ce qui indique qu’un nouveau type de modification s’est produit. La séquence d’enregistrements donne un historique partiel du fichier. L’enregistrement final, créé lorsque le fichier est fermé, ajoute l' \_ indicateur de fermeture de raison USN \_ . Cet enregistrement représente un résumé des modifications apportées au fichier, mais contrairement aux enregistrements précédents, ne donne aucune indication de l’ordre des modifications.

L’utilisateur suivant qui accède au fichier et le modifie génère un nouvel enregistrement USN avec un seul indicateur de raison.

 

 




