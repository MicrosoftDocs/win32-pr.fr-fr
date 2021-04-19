---
description: Le système de fichiers NTFS associe un identificateur non signé 64 bits à chaque journal des modifications.
ms.assetid: 5ae79460-b69a-4901-a417-1d5358dcba29
title: Utilisation de l’identificateur du journal des modifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692acf98403e45b6bdafd3cd4791a64dd1beb532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527795"
---
# <a name="using-the-change-journal-identifier"></a>Utilisation de l’identificateur du journal des modifications

Le système de fichiers NTFS associe un identificateur non signé 64 bits à chaque journal des modifications. Le journal est marqué avec cet identificateur lors de sa création. Le système de fichiers marque le journal avec un nouvel identificateur dans lequel les enregistrements de numéro de séquence de mise à jour (USN) existants sont ou peuvent être inutilisables.

Par exemple, le système de fichiers NTFS réestampille un journal des modifications avec un nouvel identificateur lorsqu’un volume est déplacé d’une version de NTFS vers une autre, puis de nouveau. Un tel déplacement peut se produire dans un environnement à double démarrage ou lors de l’utilisation d’un support amovible.

Pour obtenir l’identificateur du journal des modifications actuel sur un volume spécifié, utilisez le code de contrôle du [**\_ \_ \_ journal USN de la requête FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) . Pour effectuer cette opération et toutes les autres opérations de journal des modifications, vous devez disposer de privilèges d’administrateur système. Autrement dit, vous devez être membre du groupe administrateurs.

Lorsqu’un administrateur supprime et recrée le journal des modifications, par exemple lorsque la valeur USN actuelle approche la valeur USN maximale possible, les valeurs USN redémarrent à partir de zéro. Lorsque le système de fichiers NTFS marque un journal avec un nouvel identificateur plutôt que de recréer le journal, il ne réinitialise pas l’USN à zéro, mais continue à partir de l’USN actuel. Dans les deux cas, toutes les USN existants sont moins que les futurs USN.

Lorsque vous avez besoin d’informations sur un ensemble spécifique d’enregistrements, utilisez le code de contrôle du [**\_ \_ \_ journal USN de la requête FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) pour obtenir l’identificateur du journal des modifications. Ensuite, utilisez le code de contrôle [**\_ \_ \_ journal USN de lecture FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) pour lire les enregistrements de journal qui vous intéressent. Le système de fichiers NTFS retourne uniquement les enregistrements qui sont valides pour le journal spécifié par l’identificateur.

Votre application a besoin des USN des enregistrements et de l’identificateur pour lire le journal. Cette exigence fournit un contrôle d’intégrité dans les cas où votre application doit ignorer les enregistrements existants dans le fichier et où les enregistrements ont été écrits dans des instances précédentes du journal pour le même volume.

Pour obtenir les enregistrements qui vous intéressent, vous devez commencer à l’enregistrement le plus ancien (c’est-à-dire avec le numéro USN le plus bas) et effectuer une analyse directe jusqu’à ce que vous trouviez le premier enregistrement qui vous intéresse.

 

 
