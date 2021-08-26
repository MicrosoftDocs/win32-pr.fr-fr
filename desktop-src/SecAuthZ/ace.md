---
description: Répertorie les types d’entrées du contrôle d’accès actuellement définis.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa93490c4cf74ac33e3b15eeb888f011f81aa2b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470985"
---
# <a name="ace"></a>MAILLOTS

Une **ACE** est une [*entrée de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) dans une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL).

Le tableau suivant répertorie les types d' **entrées** du contrôle d’accès actuellement définis.




| Type d’entrée de contrôle d’accès | Structure | Type ACL | 
|----------|-----------|----------|
| <ul><li>Accès autorisé</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a> | Discrétionnaire | 
| <ul><li>Accès autorisé</li><li>Autorise le rappel lors de la vérification de l’accès</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a> | Discrétionnaire | 
| <ul><li>Accès autorisé</li><li>Spécifique à l’objet</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a> | Discrétionnaire | 
| <ul><li>Accès autorisé</li><li>Spécifique à l’objet</li><li>Autorise le rappel lors de la vérification de l’accès</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a> | Discrétionnaire | 
| <ul><li>Accès refusé</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a> | Discrétionnaire | 
| <ul><li>Accès refusé</li><li>Autorise le rappel lors de la vérification de l’accès</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a> | Discrétionnaire | 
| <ul><li>Accès refusé</li><li>Spécifique à l’objet</li><li>Autorise le rappel lors de la vérification de l’accès</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a> | Discrétionnaire | 
| <ul><li>Accès refusé</li><li>Spécifique à l’objet</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a> | Discrétionnaire | 
| <ul><li>Alarme système</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a> | Système | 
| <ul><li>Alarme système</li><li>Autorise le rappel lors de la vérification de l’accès</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a> | Système | 
| <ul><li>Alarme système</li><li>Spécifique à l’objet</li><li>Autorise le rappel lors de la vérification de l’accès</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a> | Système | 
| <ul><li>Alarme système</li><li>Spécifique à l’objet</li></ul> | <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a> | Système | 
| <ul><li>Audit du système</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a> | Système | 
| <ul><li>Audit du système</li><li>Autorise le rappel lors de la vérification de l’accès</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a> | Système | 
| <ul><li>Audit du système</li><li>Spécifique à l’objet</li><li>Autorise le rappel lors de la vérification de l’accès</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a> | Système | 
| <ul><li>Audit du système</li><li>Spécifique à l’objet</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a> | Système | 




 

Les ACE d’alarme système propre à l’objet et à l’alarme système ne sont pas prises en charge actuellement.

> [!Note]  
> Chaque entrée du contrôle d’accès commence par une structure d' [**\_ en-tête ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . Le format des données suivant l’en-tête varie en fonction du type d’entrée du contrôle d’accès spécifié dans l’en-tête.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>winnt. h (inclure Windows. h)</dt> </dl> |



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

