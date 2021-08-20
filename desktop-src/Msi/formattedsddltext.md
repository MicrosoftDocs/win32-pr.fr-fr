---
description: Un champ de base de données du type de données FormattedSDDLText contient une chaîne de texte qui décrit un descripteur de sécurité à l’aide du langage SDDL (Security Descriptor Definition Language) valide. Ce type de données est utilisé par le champ SDDLText de la table MsiLockPermissionsEx pour sécuriser un objet sélectionné. Notez que le champ SDDLText de la table MsiLockPermissionsEx ne prend pas en charge les propriétés privées ou publiques.
ms.assetid: a36e257d-ef3c-45db-a50e-94d7fd4e09e2
title: FormattedSDDLText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdfc4446c4362646e8c275ec427f759b8aec6a257d5221926431434688b91c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142888"
---
# <a name="formattedsddltext"></a>FormattedSDDLText

Un champ de base de données du type de données **FormattedSDDLText** contient une chaîne de texte qui décrit un descripteur de sécurité à l’aide du langage SDDL ( [Security Descriptor Definition Language](../secauthz/security-descriptor-definition-language.md) ) valide. Ce type de données est utilisé par le champ SDDLText de la [table MsiLockPermissionsEx](msilockpermissionsex-table.md) pour sécuriser un objet sélectionné. Notez que le champ SDDLText de la table MsiLockPermissionsEx ne prend pas en charge les propriétés privées ou publiques.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. ce type de données est disponible à partir de Windows Installer 5,0.

Le type de données **FormattedSDDLText** peut contenir une chaîne SDDL écrite dans un [format de chaîne de descripteur de sécurité](../secauthz/security-descriptor-string-format.md)valide. pour plus d’informations sur le langage SDDL, consultez la section [Access Control](../secauthz/access-control.md) du [kit de développement logiciel (SDK) de Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/). En outre, une chaîne de texte **FormattedSDDLText** peut utiliser des crochets pointus (<>) pour contenir le domaine et le nom d’utilisateur de l’utilisateur dont le SID de compte doit être déterminé.

si l’utilisateur ayant le nom d’utilisateur *SampleUser* appartient à un domaine nommé *SampleDomain*, la valeur **FormattedSDDLText** peut identifier le propriétaire à l’aide de la chaîne SID, du nom d’utilisateur et du nom de domaine, ou des variables d’environnement Windows. Par exemple, les chaînes suivantes sont possibles.

<dl> O :*propriétaire de la \_ \_ chaîne sid* G :Bad : (D ; oici ; GA ;;; BG) (A ; OICI ; GRGWGX ;;; *\_ \_ chaîne SID du propriétaire*) (A ; oici ; GA ;;; BA) S :ARAI (AU ; SAFA ;;;; WD  
O : <*SampleDomain \\ SAMPLEUSER*>G :Bad : (D ; oici ; GA ;;; BG) (A ; OICI ; GRGWGX ;;; <*SampleDomain \\ SampleUser*>) (A ; oici ; GA ;;; BA) S :ARAI (AU ; SAFA ;;;; WD  
O : <\[ % UserDomain \] \\ \[ % UserName \]>G :Bad : (D ; oici ; GA ;;; BG) (A ; OICI ; GRGWGX ;;; <\[ % UserDomain \] \\ \[ % UserName \]>) (A ; oici ; GA ;;; BA) S :ARAI (AU ; SAFA ;;;; WD
</dl>

 

 
