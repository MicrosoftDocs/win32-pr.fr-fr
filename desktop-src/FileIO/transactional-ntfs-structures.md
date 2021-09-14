---
description: Structures NTFS (TxF) transactionnelles.
ms.assetid: 85b3cf8e-bff3-4693-b00e-64bf5d1f5065
title: Structures TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d490f608ef9ebfa6906d1acffa374a0c9327489b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009819"
---
# <a name="txf-structures"></a>Structures TxF

NTFS transactionnel (TxF) fournit les structures suivantes.

## <a name="in-this-section"></a>Dans cette section



| Structure                                                                                                    | Description                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TXFS \_ créer \_ des \_ informations MINIVERSION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_create_miniversion_info)<br/>                           | Contient les informations de version sur le miniversion créé par [**FSCTL \_ TXFS \_ Create \_ miniversion**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion).<br/>                                            |
| [**TXFS \_ de \_ récupérer \_ les informations de métadonnées \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_metadata_info_out)<br/>                              | Contient les informations de version sur le miniversion créé.<br/>                                                                                                                 |
| [**\_ID TxF**](/windows/desktop/api/TxfW32/ns-txfw32-txf_id)<br/>                                                                         | Représente un identificateur unique dans le contexte de l’Gestionnaire des ressources.<br/>                                                                                                              |
| [**TXFS \_ recevoir la \_ \_ version transactionnelle**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_transacted_version)<br/>                             | Contient les informations sur les versions de base et les dernières versions du fichier spécifié.<br/>                                                                                                      |
| [**\_liste TXFS \_ \_ fichiers verrouillés de transaction \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files)<br/>              | Contient la liste des fichiers verrouillés par un rédacteur transactionnel.<br/>                                                                                                                                 |
| [**\_entrée TXFS liste des \_ \_ fichiers verrouillés de transaction \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files_entry)<br/> | Contient des informations sur une transaction verrouillée.<br/>                                                                                                                                        |
| [**\_transactions de liste TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions)<br/>                                        | Contient une liste de transactions.<br/>                                                                                                                                                        |
| [**entrée de la \_ liste des \_ transactions TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions_entry)<br/>                           | Contient des informations sur une transaction.<br/>                                                                                                                                               |
| [**\_fichier d’enregistrement du journal TxF \_ \_ affecté \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_affected_file)<br/>                          | Contient des informations relatives à un fichier qui a été affecté par une transaction.<br/>                                                                                                                     |
| [**\_base d' \_ enregistrement de journal TxF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_base)<br/>                                             | Contient les informations d’enregistrement de base.<br/>                                                                                                                                                  |
| [**l' \_ enregistrement de journal TxF est \_ \_ tronqué**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_truncate)<br/>                                     | Contient l’enregistrement d’une opération de troncation.<br/>                                                                                                                                           |
| [**TXF \_ \_ écriture d’enregistrement de journal \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_write)<br/>                                           | Contient l’enregistrement d’une opération d’écriture.<br/>                                                                                                                                              |
| [**TXFS \_ modifier \_ RM**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_modify_rm)<br/>                                                        | Contient les informations requises lors de la modification des paramètres de journalisation et du mode de journalisation pour un gestionnaire de ressources secondaire.<br/>                                                                      |
| [**\_ \_ informations sur le gestionnaire de requêtes TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_query_rm_information)<br/>                                 | Contient des informations sur le gestionnaire de ressources (RM).<br/>                                                                                                                                   |
| [**TXFS \_ lire \_ \_ les informations de sauvegarde \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/>                  | Contient une structure spécifique NTFS (TxF) transactionnelle. Ces informations ne doivent être utilisées que lors de l’appel d' [**\_ informations de \_ sauvegarde \_ d’écriture TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information).<br/>    |
| [**TXFS \_ les \_ informations sur le point d’enregistrement**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information)<br/>                                | La structure d’informations de point d’enregistrement [**FSCTL \_ TXFS \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information) spécifie l’action à effectuer et sur quelle transaction.<br/>                                      |
| [**\_ \_ informations actives de la transaction TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_transaction_active_info)<br/>                           | Contient l’indicateur qui indique si les transactions étaient actives ou non lorsqu’un instantané a été pris.<br/>                                                                                     |
| [**TXFS \_ écrire \_ les \_ informations de sauvegarde**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>                         | Contient une structure spécifique NTFS (TxF) transactionnelle. Ces informations ne doivent être utilisées que lors de l’appel d' [**\_ informations de \_ sauvegarde \_ d’écriture TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out).<br/> |



 

 

