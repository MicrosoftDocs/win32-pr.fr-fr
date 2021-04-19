---
description: Répertorie les types d’entrées du contrôle d’accès actuellement définis.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d06b3457e4df6aea38d3e35acf4f7aaa4e2f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525015"
---
# <a name="ace"></a>MAILLOTS

Une **ACE** est une [*entrée de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) dans une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL).

Le tableau suivant répertorie les types d' **entrées** du contrôle d’accès actuellement définis.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Type d’entrée de contrôle d’accès</th>
<th>Structure</th>
<th>Type ACL</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Accès autorisé</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></td>
<td>Discrétionnaire</td>
</tr>
<tr class="even">
<td><ul>
<li>Accès autorisé</li>
<li>Autorise le rappel lors de la vérification de l’accès</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></td>
<td>Discrétionnaire</td>
</tr>
<tr class="odd">
<td><ul>
<li>Accès autorisé</li>
<li>Spécifique à l’objet</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></td>
<td>Discrétionnaire</td>
</tr>
<tr class="even">
<td><ul>
<li>Accès autorisé</li>
<li>Spécifique à l’objet</li>
<li>Autorise le rappel lors de la vérification de l’accès</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Discrétionnaire</td>
</tr>
<tr class="odd">
<td><ul>
<li>Accès refusé</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></td>
<td>Discrétionnaire</td>
</tr>
<tr class="even">
<td><ul>
<li>Accès refusé</li>
<li>Autorise le rappel lors de la vérification de l’accès</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></td>
<td>Discrétionnaire</td>
</tr>
<tr class="odd">
<td><ul>
<li>Accès refusé</li>
<li>Spécifique à l’objet</li>
<li>Autorise le rappel lors de la vérification de l’accès</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Discrétionnaire</td>
</tr>
<tr class="even">
<td><ul>
<li>Accès refusé</li>
<li>Spécifique à l’objet</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></td>
<td>Discrétionnaire</td>
</tr>
<tr class="odd">
<td><ul>
<li>Alarme système</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></td>
<td>Système</td>
</tr>
<tr class="even">
<td><ul>
<li>Alarme système</li>
<li>Autorise le rappel lors de la vérification de l’accès</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></td>
<td>Système</td>
</tr>
<tr class="odd">
<td><ul>
<li>Alarme système</li>
<li>Spécifique à l’objet</li>
<li>Autorise le rappel lors de la vérification de l’accès</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Système</td>
</tr>
<tr class="even">
<td><ul>
<li>Alarme système</li>
<li>Spécifique à l’objet</li>
</ul></td>
<td><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></td>
<td>Système</td>
</tr>
<tr class="odd">
<td><ul>
<li>Audit du système</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></td>
<td>Système</td>
</tr>
<tr class="even">
<td><ul>
<li>Audit du système</li>
<li>Autorise le rappel lors de la vérification de l’accès</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></td>
<td>Système</td>
</tr>
<tr class="odd">
<td><ul>
<li>Audit du système</li>
<li>Spécifique à l’objet</li>
<li>Autorise le rappel lors de la vérification de l’accès</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Système</td>
</tr>
<tr class="even">
<td><ul>
<li>Audit du système</li>
<li>Spécifique à l’objet</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></td>
<td>Système</td>
</tr>
</tbody>
</table>



 

Les ACE d’alarme système propre à l’objet et à l’alarme système ne sont pas prises en charge actuellement.

> [!Note]  
> Chaque entrée du contrôle d’accès commence par une structure d' [**\_ en-tête ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . Le format des données suivant l’en-tête varie en fonction du type d’entrée du contrôle d’accès spécifié dans l’en-tête.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Winnt. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[**ACCÈS \_ ACE autorisé pour l’accès \_**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[**ACCÈS \_ refusé \_**](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[**\_ACE d’alarme système \_**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[**\_ACE d’audit système \_**](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

