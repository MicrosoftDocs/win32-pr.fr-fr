---
title: Listes de Access Control pour COM
description: Listes de Access Control pour COM
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811b6cdbca36ef75bb5ee3f185b0261967d736d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120442"
---
# <a name="access-control-lists-for-com"></a>Listes de Access Control pour COM

Windows server XP service pack 2 (sp2) et Windows server 2003 service pack 1 (sp 1) présentent des améliorations de sécurité pour le modèle DCOM (Distributed Component Object Model). L’une de ces améliorations est l’utilisation de droits d’accès plus spécifiques dans les listes de contrôle d’accès (ACL). Les droits d’accès sont les suivants :

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

pour assurer la compatibilité descendante, une liste de contrôle d’accès peut exister au format utilisé avant Windows XP sp 2 et Windows Server 2003 sp 1, qui utilise uniquement les droits com d’accès qui \_ \_ s’exécutent, ou il peut exister dans le nouveau format utilisé dans Windows XP sp 2 et Windows Server 2003 sp 1, qui utilise des \_ droits com \_ s’exécutent avec une combinaison de \_ droits com \_ exécuter \_ local, les \_ droits com \_ exécuter \_ à distance, les \_ droits com \_ activent \_ les droits locaux et les \_ droits com \_ activer \_ à distance.

> [!Note]  
> \_ \_ L’exécution des droits com doit toujours être présente ; l’absence de ce droit génère un descripteur de sécurité non valide.

 

Vous ne devez pas mélanger l’ancien format et le nouveau format dans une ACL unique. toutes les entrées de contrôle d’accès (ACE, Access Control Entry) doivent accorder uniquement le \_ \_ droit d’accès d’exécution des droits com, ou elles doivent toutes accorder des \_ droits com \_ en association avec une combinaison de \_ droits com \_ Execute \_ local, les \_ droits com \_ Execute \_ Remote, les \_ droits com \_ active \_ locale et les \_ droits com \_ Activate \_ Remote.

Voici un exemple de liste de contrôle d’accès mal mise en forme :

``` syntax
Revision 1
Sbz1 0
Control 0x8004
    SE_DACL_PRESENT
    SE_SELF_RELATIVE
Owner: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
Group: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
DACL:
    AclRevision 2
    Sbz1 0
    AclSize 128
    AceCount 4
    Sbz2 0
    Ace[0]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 36
        AccessMask 0x1
        S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
    Ace[1]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0xb
        S-1-5-18 (Well Known Group: NT AUTHORITY\SYSTEM)
    Ace[2]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0x9
        S-1-5-11 (Well Known Group: NT AUTHORITY\Authenticated Users)
SACL:
    (null)
```

Notez que la première entrée de contrôle d’accès (ACE, Access Control Entry) accorde des \_ droits com \_ Execute (0x1) uniquement, tandis que la deuxième ACE accorde des \_ droits com \_ Execute, les \_ droits com \_ Execute \_ local et \_ les droits com \_ Activate local \_ (0xB), tandis que la troisième accorde les droits com \_ \_ Execute et les \_ droits com \_ active \_ local (0x9).

Pour corriger cela, la première entrée du contrôle d’accès doit être modifiée pour permettre l' \_ exécution des droits com \_ en association avec l’un des quatre autres droits d’accès, sinon les deuxième et troisième entrées de contrôle d’accès doivent être modifiées pour permettre l’exécution des droits com uniquement \_ \_ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[améliorations de la sécurité DCOM dans Windows XP service pack 2 et Windows Server 2003 service pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 




