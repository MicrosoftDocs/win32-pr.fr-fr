---
description: Le NTFS transactionnel (TxF) intègre des transactions dans le système de fichiers NTFS, ce qui permet aux développeurs d’applications et aux administrateurs de gérer plus facilement les erreurs et de préserver l’intégrité des données.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: À propos du NTFS transactionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318433"
---
# <a name="about-transactional-ntfs"></a>À propos du NTFS transactionnel

\[Microsoft recommande vivement aux développeurs d’utiliser d’autres moyens pour répondre aux besoins de votre application. De nombreux scénarios pour lesquels TxF a été développé peuvent être obtenus à l’aide de techniques plus simples et plus facilement disponibles. En outre, TxF peut ne pas être disponible dans les versions futures de Microsoft Windows. Pour plus d’informations et pour obtenir des alternatives à TxF, consultez [alternatives à l’utilisation de NTFS transactionnel](deprecation-of-txf.md).\]

Le NTFS transactionnel (TxF) intègre des transactions dans le système de fichiers NTFS, ce qui permet aux développeurs d’applications et aux administrateurs de gérer plus facilement les erreurs et de préserver l’intégrité des données.

TxF peut participer aux transactions distribuées que les coordonnées [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) , ce qui vous permet d’utiliser TxF pour les éléments suivants :

-   Transactions qui s’étendent sur plusieurs magasins de données, par exemple une transaction unique pour les opérations de fichier et SQL
-   Transactions qui s’étendent sur plusieurs ordinateurs, par exemple, une seule transaction pour les mises à jour de fichiers sur plusieurs ordinateurs

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                 | Description                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Quand utiliser le NTFS transactionnel](when-to-use-transactional-ntfs.md)<br/>                                       | Utilisez le NTFS transactionnel pour maintenir l’intégrité des données.<br/>                                                                        |
| [Déploiement de NTFS transactionnel](deploying-transactional-ntfs.md)<br/>                                           | Contrôle de la mise en cache dans le NTFS transactionnel.<br/>                                                                                    |
| [Utilisation de NTFS transactionnel](how-to-use-transactional-ntfs.md)<br/>                                         | Gestion des descripteurs de fichiers transactionnels dans NTFS transactionnel.<br/>                                                                   |
| [Concepts de base de TxF](txf-basic-concepts.md)<br/>                                                               | Décrit la cohérence des lectures validées, l’isolation de lecture validée et les concepts de verrouillage transactionnel dans NTFS transactionnel.<br/> |
| [Considérations relatives à la programmation pour NTFS transactionnel](programming-considerations-for-transacted-fileio-.md)<br/> | Décrit les différentes considérations en matière de programmation pour le NTFS transactionnel.<br/>                                                      |
| [Considérations relatives aux performances pour le NTFS transactionnel](performance-considerations-for-transactional-ntfs.md)<br/> | Recommandations pour les transactions de système de fichiers optimales.<br/>                                                                     |



 

 

