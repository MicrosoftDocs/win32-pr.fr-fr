---
title: Codes d’erreur SNMP (SNMP. h)
description: Microsoft implémente les codes d’erreur SNMP suivants qui sont définis par la spécification SNMPv2C.
ms.assetid: 7e7e2bc0-a058-4853-b736-1946e64a0c4a
topic_type:
- apiref
api_name:
- SNMP_ERRORSTATUS_NOERROR
- SNMP_ERRORSTATUS_TOOBIG
- SNMP_ERRORSTATUS_NOSUCHNAME
- SNMP_ERRORSTATUS_BADVALUE
- SNMP_ERRORSTATUS_READONLY
- SNMP_ERRORSTATUS_GENERR
- SNMP_ERRORSTATUS_NOACCESS
- SNMP_ERRORSTATUS_WRONGTYPE
- SNMP_ERRORSTATUS_WRONGLENGTH
- SNMP_ERRORSTATUS_WRONGENCODING
- SNMP_ERRORSTATUS_WRONGVALUE
- SNMP_ERRORSTATUS_NOCREATION
- SNMP_ERRORSTATUS_INCONSISTENTVALUE
- SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE
- SNMP_ERRORSTATUS_COMMITFAILED
- SNMP_ERRORSTATUS_UNDOFAILED
- SNMP_ERRORSTATUS_AUTHORIZATIONERROR
- SNMP_ERRORSTATUS_NOTWRITABLE
- SNMP_ERRORSTATUS_INCONSISTENTNAME
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583394dfc3093f4f0d5cf3d7c7cef68d7ff6d57930e3abf957d857defec227c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008927"
---
# <a name="snmp-error-codes"></a>Codes d’erreur SNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

Microsoft implémente les codes d’erreur SNMP suivants qui sont définis par la spécification SNMPv2C.



| Constante/valeur                                                                                                                                                                                                                                                                              | Description                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_ERRORSTATUS_NOERROR"></span><span id="snmp_errorstatus_noerror"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ noerreur**</dt> <dt>0</dt> </dl>                                      | L’agent signale qu’aucune erreur ne s’est produite au cours de la transmission.<br/>                                                                                      |
| <span id="SNMP_ERRORSTATUS_TOOBIG"></span><span id="snmp_errorstatus_toobig"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ TOOBIG**</dt> <dt>1</dt> </dl>                                         | L’agent n’a pas pu placer les résultats de l’opération SNMP demandée dans un seul message SNMP.<br/>                                                     |
| <span id="SNMP_ERRORSTATUS_NOSUCHNAME"></span><span id="snmp_errorstatus_nosuchname"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ NOSUCHNAME**</dt> <dt>2</dt> </dl>                             | L’opération SNMP demandée a identifié une variable inconnue.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_BADVALUE"></span><span id="snmp_errorstatus_badvalue"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ BADVALUE**</dt> <dt>3</dt> </dl>                                   | L’opération SNMP demandée a tenté de modifier une variable, mais elle spécifiait une erreur de syntaxe ou de valeur.<br/>                                            |
| <span id="SNMP_ERRORSTATUS_READONLY"></span><span id="snmp_errorstatus_readonly"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ ReadOnly**</dt> <dt>4</dt> </dl>                                   | L’opération SNMP demandée a tenté de modifier une variable qui n’était pas autorisée à changer, selon le profil communautaire de la variable.<br/>         |
| <span id="SNMP_ERRORSTATUS_GENERR"></span><span id="snmp_errorstatus_generr"></span><dl> <dt>**Protocole SNMP \_ \_Genre de ERRORSTATUS**</dt> <dt>5</dt> </dl>                                         | Une erreur autre que celle répertoriée ici s’est produite au cours de l’opération SNMP demandée.<br/>                                                          |
| <span id="SNMP_ERRORSTATUS_NOACCESS"></span><span id="snmp_errorstatus_noaccess"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ NoAccess**</dt> <dt>6</dt> </dl>                                   | La variable SNMP spécifiée n’est pas accessible.<br/>                                                                                                      |
| <span id="SNMP_ERRORSTATUS_WRONGTYPE"></span><span id="snmp_errorstatus_wrongtype"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ WRONGTYPE**</dt> <dt>7</dt> </dl>                                | La valeur spécifie un type qui n’est pas cohérent avec le type requis pour la variable.<br/>                                                            |
| <span id="SNMP_ERRORSTATUS_WRONGLENGTH"></span><span id="snmp_errorstatus_wronglength"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ WRONGLENGTH**</dt> <dt>8</dt> </dl>                          | La valeur spécifie une longueur qui est incohérente avec la longueur requise pour la variable.<br/>                                                        |
| <span id="SNMP_ERRORSTATUS_WRONGENCODING"></span><span id="snmp_errorstatus_wrongencoding"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ WRONGENCODING**</dt> <dt>9</dt> </dl>                    | La valeur contient un encodage ASN. 1 (Abstract Syntax Notation One) qui est incohérent avec la balise ASN. 1 du champ.<br/>                           |
| <span id="SNMP_ERRORSTATUS_WRONGVALUE"></span><span id="snmp_errorstatus_wrongvalue"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ WRONGVALUE**</dt> <dt>10</dt> </dl>                            | La valeur ne peut pas être assignée à la variable.<br/>                                                                                                       |
| <span id="SNMP_ERRORSTATUS_NOCREATION"></span><span id="snmp_errorstatus_nocreation"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ nocréation**</dt> <dt>11</dt> </dl>                            | La variable n’existe pas et l’agent ne peut pas la créer.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTVALUE"></span><span id="snmp_errorstatus_inconsistentvalue"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ INCONSISTENTVALUE**</dt> <dt>12</dt> </dl>       | La valeur est incohérente avec les valeurs d’autres objets managés.<br/>                                                                                     |
| <span id="SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE"></span><span id="snmp_errorstatus_resourceunavailable"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ RESOURCEUNAVAILABLE**</dt> <dt>13</dt> </dl> | L’attribution de la valeur à la variable requiert l’allocation des ressources qui ne sont pas disponibles actuellement.<br/>                                                |
| <span id="SNMP_ERRORSTATUS_COMMITFAILED"></span><span id="snmp_errorstatus_commitfailed"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ COMMITFAILED**</dt> <dt>14</dt> </dl>                      | Aucune erreur de validation ne s’est produite, mais aucune variable n’a été mise à jour.<br/>                                                                                       |
| <span id="SNMP_ERRORSTATUS_UNDOFAILED"></span><span id="snmp_errorstatus_undofailed"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ UNDOFAILED**</dt> <dt>15</dt> </dl>                            | Aucune erreur de validation ne s’est produite. Certaines variables ont été mises à jour, car il n’était pas possible d’annuler leur affectation.<br/>                                    |
| <span id="SNMP_ERRORSTATUS_AUTHORIZATIONERROR"></span><span id="snmp_errorstatus_authorizationerror"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ AUTHORIZATIONERROR**</dt> <dt>16</dt> </dl>    | Une erreur d’autorisation s’est produite.<br/>                                                                                                                    |
| <span id="SNMP_ERRORSTATUS_NOTWRITABLE"></span><span id="snmp_errorstatus_notwritable"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ NOTWRITABLE**</dt> <dt>17</dt> </dl>                         | La variable existe, mais l’agent ne peut pas la modifier.<br/>                                                                                                 |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTNAME"></span><span id="snmp_errorstatus_inconsistentname"></span><dl> <dt>**Protocole SNMP \_ ERRORSTATUS \_ INCONSISTENTNAME**</dt> <dt>18</dt> </dl>          | La variable n’existe pas ; l’agent ne peut pas le créer, car l’instance de l’objet nommé n’est pas cohérente avec les valeurs d’autres objets managés.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                        |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>SNMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du protocole SNMP (Simple Network Management Protocol)](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[Référence SNMP](snmp-reference.md)
</dt> </dl>

 

