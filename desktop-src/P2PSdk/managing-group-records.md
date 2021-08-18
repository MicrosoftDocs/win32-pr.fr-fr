---
description: Un enregistrement de groupe est une donnée spécifique publiée à tous les membres actifs d’un groupe homologue, par exemple un message de conversation ou une mise à jour d’état spécifique à l’application.
ms.assetid: 073ee4e9-0e97-451a-a808-8265575d073c
title: Gestion des enregistrements de groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2d0ba77a315043e638ddaa28615cf84654852a13e73347ee36ee4c7d66a6e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061397"
---
# <a name="managing-group-records"></a>Gestion des enregistrements de groupe

Un enregistrement de groupe est une donnée spécifique publiée à tous les membres actifs d’un groupe homologue, par exemple un message de conversation ou une mise à jour d’état spécifique à l’application. Un enregistrement est représenté par la structure de l' [**\_ enregistrement homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) et contient les informations suivantes sur un homologue :

-   L’ID d’enregistrement est une valeur qui identifie de façon unique un enregistrement dans le groupe homologue.
-   GUID qui spécifie le type d’enregistrement. Les applications peuvent prendre en charge différents types d’enregistrements. Une application interprète le champ de **données** d’un enregistrement en fonction du type d’enregistrement. Certains GUID sont réservés, et l’appel d’API retourne l' **homologue \_ E \_ non \_ autorisé** lorsque l’application tente de les utiliser.
-   Ensemble d’attributs d’enregistrement décrits comme une chaîne XML. Les attributs sont utilisés lors de la recherche d’enregistrements. Pour plus d’informations sur les attributs, consultez [enregistrement du schéma d’attribut](record-attribute-schema.md).
-   Heure d’homologue à laquelle un enregistrement est créé.
-   Temps d’homologation d’expiration d’un enregistrement.
-   Temps d’attente de modification d’un enregistrement.
-   Créateur d’un enregistrement.
-   Membre qui modifie un enregistrement.
-   Structure [**de \_ données d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_data) qui contient la signature de chiffrement pour tous les champs de cette structure d' [**\_ enregistrement d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Ce champ ne peut pas être directement mis à jour ou modifié par un homologue.
-   Structure [**de \_ données d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_data) qui contient les données spécifiques à l’application associées à cet enregistrement sous la forme d’un tableau d’octets. Le type de données présent dans ce champ est déterminé par le type d’enregistrement défini par l’application.

## <a name="obtaining-peer-group-records"></a>Obtention d’enregistrements de groupe homologue

Les enregistrements individuels sont obtenus en appelant [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) avec l’ID de l’enregistrement. Lors du traitement de tous les enregistrements d’un type spécifique, l’ensemble énuméré de tous les enregistrements du groupe homologue actuel est obtenu en appelant [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords) pour ouvrir l’énumération, puis en appelant de manière itérative [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) jusqu’à ce que tous les enregistrements soient récupérés. Lorsque vous avez terminé, fermez l’énumération et libérez la mémoire qui lui est associée en appelant [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

Lorsqu’un enregistrement est créé, supprimé ou mis à jour par un homologue, l’enregistrement affecté est publié sur tous les membres du groupe homologue par le biais de l’événement de modification de l' **\_ enregistrement d’événement du groupe \_ \_ \_ pair** . Notez que si un homologue n’est pas connecté au groupe, il recevra l’enregistrement mis à jour, puis la prochaine fois qu’il se connectera. Il est important de s’inscrire à cet événement avec [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) si votre application gère ou gère les enregistrements de manière explicite. L’application peut également interroger la base de données d’enregistrement à la demande à l’aide de [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords).

Lorsque l’événement de **modification d’enregistrement d' \_ événement de groupe \_ \_ \_ pair** est déclenché, l’ID d’enregistrement et le type spécifiques, ainsi que le type de modification (ajout, mise à jour, suppression) sont reçus comme une structure de [**données de modification d' \_ enregistrement d’événement \_ \_ \_ homologue**](/windows/desktop/api/P2P/ns-p2p-peer_event_record_change_data) . Cette structure est obtenue à l’aide d’un appel à [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Si la modification est un ajout ou une mise à jour, vous devez utiliser [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) pour obtenir l’enregistrement avec l’ID fourni. La base de données d’enregistrement locale pour l’infrastructure est mise à jour automatiquement.

Vous pouvez également rechercher des enregistrements spécifiques en fonction d’attributs personnalisés spécifiques fournis dans le champ **pwzAttributes** de l' [**\_ enregistrement homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record), ainsi que de tous les attributs prédéfinis. Pour ce faire, utilisez la fonction [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) avec une requête de recherche XML mise en forme comme spécifié dans la rubrique [format de requête de recherche d’enregistrements](record-search-query-format.md) .

Pour plus d’informations sur l’utilisation des enregistrements dans l’infrastructure homologue, reportez-vous à la rubrique relative aux [enregistrements](records.md) dans [utilisation de l’infrastructure homologue](using-the-peer-infrastructure.md).

## <a name="administration-of-peer-group-records"></a>Administration des enregistrements de groupe homologue

Lorsque les invitations initiales sont émises par le créateur du groupe pair, il peut spécifier que certains membres jouent un rôle d’administrateur (administrateur du rôle de groupe HOMOLOGUe \_ \_ \_ ) chaque fois qu’il envoie de nouvelles informations d’identification à l’utilisateur (via [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) ou [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)). Un administrateur a la possibilité d’ajouter, de supprimer et de mettre à jour directement les enregistrements de groupe homologue. À l’inverse, un membre du groupe homologue dont le rôle est défini sur membre du **\_ rôle de groupe \_ \_ homologue** ou **membre d’invitation du \_ \_ rôle de \_ \_ groupe** pair peut uniquement ajouter, mettre à jour et supprimer ses propres enregistrements.

Le créateur a le rôle d’administrateur par défaut.

Pour mettre à jour un enregistrement, obtenez l’enregistrement avec [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) ou [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords), effectuez les modifications et transmettez l’enregistrement mis à jour à [**PeerGroupUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord).

Pour supprimer un enregistrement, transmettez l’ID d’enregistrement à supprimer à [**PeerGroupDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord).

Pour ajouter un enregistrement, créez une nouvelle structure d' [**\_ enregistrement d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) et remplissez les champs suivants :

-   **dwSize nul**. Ce champ contient la valeur de **sizeof**([**\_ enregistrement d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record)).
-   **ftExpiration**. Ce champ contient la date et l’heure d’expiration de cet enregistrement, exprimées en temps d’homologation sous la forme d’une structure **fileTime** .
-   **tapez**. Ce champ contient une valeur **GUID** qui identifie le type d’enregistrement à l’application. Si ce type est personnalisé pour votre infrastructure d’application, vous devez également renseigner le champ de **données** .

Les champs suivants sont remplis par l’infrastructure et sont ignorés s’ils sont définis par l’application :

-   **id**
-   **pwzCreatorId**
-   **pwzLastModifiedById**
-   **ftCreation**
-   **ftLastModified**
-   **securityData**

Les champs restants sont facultatifs. Pour ajouter ce nouvel enregistrement au groupe homologue, transmettez-le à [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord).

## <a name="importing-and-exporting-records"></a>Importation et exportation d’enregistrements

Les enregistrements de groupe d’égal à égal sont conservés localement en tant que base de données. Pour enregistrer un instantané actuel de la base de données de l’enregistrement du groupe homologue dans un fichier local, appelez [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)et transmettez-lui le descripteur du groupe homologue. Ce fichier peut ensuite être transporté vers un autre ordinateur ou une autre application, qui peut extraire et utiliser cette base de données d’enregistrement en appelant [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase).

 

 



