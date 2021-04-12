---
description: Fournit les méthodes nécessaires pour construire et gérer une unité de données de protocole de carte à puce (APDU).
ms.assetid: fd84bb2e-27da-4670-b8e8-56c7948b78bb
title: Interface ISCardCmd (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd
- ISCardCmd.Type
- ISCardCmd.get_Type
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f14291f3777dcdc8b661f96f94d987209100a365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033860"
---
# <a name="iscardcmd-interface"></a>Interface ISCardCmd

\[L’interface **ISCardCmd** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

L’interface **ISCardCmd** fournit les méthodes nécessaires pour construire et gérer une [*unité de données de protocole*](../secgloss/a-gly.md) de [*carte à puce*](../secgloss/s-gly.md) (APDU). Cette interface encapsule deux mémoires tampons :

-   La mémoire tampon APDU contient la séquence de commandes qui sera envoyée à la carte.
-   La mémoire tampon APDUReply contient les données retournées par la carte après l’exécution de la commande APDU (ces données sont également appelées APDU de retour).

L’exemple suivant illustre une utilisation type de l’interface **ISCardCmd** . L’interface **ISCardCmd** est utilisée pour générer un APDU.

**Pour soumettre une transaction à une carte spécifique**

1.  Créez une interface [**ISCard**](iscard.md) et connectez-vous à une carte à puce.
2.  Créer une interface **ISCardCmd** .
3.  Générez une commande APDU de carte à puce à l’aide de l’interface [**ISCardISO7816**](iscardiso7816.md) ou de l’une des méthodes de génération **ISCardCmd** .
4.  Exécutez la commande sur la carte à puce en appelant la méthode d’interface [**ISCard**](iscard.md) appropriée.
5.  Évaluez la réponse retournée.
6.  Répétez la procédure si nécessaire.
7.  Libérez l’interface **ISCardCmd** et d’autres en fonction des besoins.

## <a name="members"></a>Membres

L’interface **ISCardCmd** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardCmd** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **ISCardCmd** possède ces méthodes.



| Méthode                                       | Description                                                                                                |
|:---------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**BuildCmd**](iscardcmd-buildcmd.md)       | Construit une commande APDU valide pour la transmission à une carte à puce.<br/>                               |
| [**Effacé**](iscardcmd-clear.md)             | Efface les mémoires tampons de messages APDU et de réponse.<br/>                                             |
| [**Encapsuler**](iscardcmd-encapsulate.md) | Encapsule la commande APDU donnée dans une autre commande APDU pour la transmettre à une carte à puce.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **ISCardCmd** possède les propriétés suivantes.



| Propriété                                                              | Type d’accès           | Description                                                                                                                                                         |
|:----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AlternateClassId**](iscardcmd-get-alternateclassid.md)<br/> | Lecture/écriture<br/> | Valeur actuelle de l’ID de classe de remplacement.<br/>                                                                                                                        |
| [**APDU**](iscardcmd-get-apdu.md)<br/>                         | Lecture/écriture<br/> | [*Unité de données de protocole d’application*](../secgloss/a-gly.md) brute (APDU).<br/> |
| [**ApduLength**](iscardcmd-get-apdulength.md)<br/>             | Lecture seule<br/>  | Longueur du APDU.<br/>                                                                                                                                      |
| [**ApduReply**](iscardcmd-get-apdureply.md)<br/>               | Lecture/écriture<br/> | [*Répondre au APDU*](../secgloss/r-gly.md).<br/>                                                                        |
| [**ApduReplyLength**](iscardcmd-get-apdureplylength.md)<br/>   | Lecture/écriture<br/> | Longueur de la réponse APDU.<br/>                                                                                                                                |
| [**ClassId**](iscardcmd-get-classid.md)<br/>                   | Lecture/écriture<br/> | ID de classe du APDU.<br/>                                                                                                                                    |
| [**Données**](iscardcmd-get-data.md)<br/>                         | Lecture seule<br/>  | Champ de données de l’APDU.<br/>                                                                                                                                  |
| [**InstructionId**](iscardcmd-get-instructionid.md)<br/>       | Lecture/écriture<br/> | Octet d’ID d’instruction issu du APDU.<br/>                                                                                                                       |
| [**LeField**](iscardcmd-get-lefield.md)<br/>                   | Lecture seule<br/>  | Champ le de la APDU.<br/>                                                                                                                                    |
| [**ADN**](iscardcmd-put-nad.md)<br/>                           | Lecture/écriture<br/> | Adresse du nœud.<br/>                                                                                                                                            |
| [**P1**](iscardcmd-get-p1.md)<br/>                             | Lecture/écriture<br/> | Premier octet de paramètre de l’APDU.<br/>                                                                                                                        |
| [**P2**](iscardcmd-get-p2.md)<br/>                             | Lecture/écriture<br/> | Deuxième octet de paramètre de l’APDU.<br/>                                                                                                                       |
| [**P3**](iscardcmd-get-p3.md)<br/>                             | Lecture seule<br/>  | Troisième octet de paramètre de l’APDU.<br/>                                                                                                                        |
| [**ReplyNad**](iscardcmd-get-replynad.md)<br/>                 | Lecture/écriture<br/> | Adresse de nœud utilisée par la carte dans le message de réponse.<br/>                                                                                                      |
| [**ReplyStatus**](iscardcmd-get-replystatus.md)<br/>           | Lecture/écriture<br/> | [*Répondre*](../secgloss/r-gly.md) au mot d’État du message APDU.<br/>                                                    |
| [**ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)<br/>     | Lecture seule<br/>  | Répondre à l’octet d’État SW1 du message APDU.<br/>                                                                                                                    |
| [**ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)<br/>     | Lecture seule<br/>  | Répondre à l’octet d’État SW2 du message APDU.<br/>                                                                                                                    |
| **Type**<br/>                                                   | Lecture seule<br/>  | Réservé pour un usage futur.<br/>                                                                                                                                 |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



 

 
