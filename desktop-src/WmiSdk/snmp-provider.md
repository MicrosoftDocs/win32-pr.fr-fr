---
description: le fournisseur SNMP (Simple Network Management Protocol) permet aux applications clientes d’accéder aux informations SNMP par le biais d’Windows Management Instrumentation (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI et SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f1327afe2a86a1f56f40c0a93d904148ccaf1fd0547b6cb623d9eb420c2a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992299"
---
# <a name="wmi-and-snmp"></a>WMI et SNMP

le fournisseur SNMP (Simple Network Management Protocol) permet aux applications clientes d’accéder aux informations SNMP par le biais d’Windows Management Instrumentation (WMI). Le fournisseur SNMP n’est pas installé par défaut. Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

Le protocole SNMP (simple Network Management Protocol) utilise un schéma pour définir des objets. Le schéma est différent du schéma utilisé dans WMI. Le schéma SNMPv1 et SNMPv2C est appelé la structure des informations de gestion (SMI) et est empaqueté en tant que fichiers MIB (Management Information base). Les fichiers MIB définissent des objets à l’aide d’un langage standard, à savoir la notation de syntaxe abstraite 1 (ASN. 1), et un certain nombre de définitions de macros qui servent de modèles pour décrire les objets. Les macros fournissent des informations telles que le nom de l’objet, l’identificateur, la syntaxe, la description, les droits d’accès, les opérations de protocole et l’encodage de protocole. Le tableau suivant répertorie la manière dont le fournisseur SNMP gère les différents aspects d’un objet MIB.



| Rubrique                                                    | Description                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [Macro de TYPE NOTIFICATION](notification-type-macro.md)   | Mappage de la macro de **type notification** de SNMP à WMI.  |
| [Macro de TYPE objet](object-type-macro.md)               | Mappage de la macro de **type objet** de SNMP à WMI.        |
| [Macro de CONVENTION textuelle](textual-convention-macro.md) | Comment la macro de **Convention textuelle** est mappée de SNMP à WMI. |
| [TYPE d’interruption (macro)](trap-type-macro.md)                   | Mappage de la macro de **type d’interruption** de SNMP à WMI.          |



 

Le fournisseur SNMP est fourni avec un compilateur qui traduit les objets MIB en objets WMI. Le compilateur SNMP peut également générer des erreurs ou d’autres messages. Pour plus d’informations, consultez [messages d’erreur du compilateur SNMP](snmp-compiler-error-messages.md) et [messages d’informations générales](general-information-messages.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence WMI](wmi-reference.md)
</dt> <dt>

[Fournisseurs WMI](wmi-providers.md)
</dt> </dl>

 

 



