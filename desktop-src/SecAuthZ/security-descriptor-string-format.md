---
description: Le format de chaîne de descripteur de sécurité est un format texte permettant de stocker ou de transporter des informations dans un descripteur de sécurité.
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: Format de chaîne de descripteur de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f5182de796ee8d3c61f079d3704ab29ad552457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863009"
---
# <a name="security-descriptor-string-format"></a>Format de chaîne de descripteur de sécurité

Le **format de chaîne de descripteur de sécurité** est un format texte permettant de stocker ou de transporter des informations dans un descripteur de sécurité. Les fonctions [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) et [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) utilisent ce format.

Le format est une chaîne se terminant par un caractère **null** avec des jetons pour indiquer chacun des quatre composants principaux d’un descripteur de sécurité : propriétaire (O :), groupe principal (G :), DACL (D :) et SACL (S :).

> [!Note]  
> Les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) et les ACE conditionnelles ont des formats différents. Pour les ACE, consultez [chaînes ACE](ace-strings.md). Pour les ACE conditionnelles, consultez [langage de définition du descripteur de sécurité pour les ACE conditionnelles](security-descriptor-definition-language-for-conditional-aces-.md).

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span id="owner_sid"></span><span id="OWNER_SID"></span>sid du propriétaire \_
</dt> <dd>

[Chaîne sid](sid-strings.md) qui identifie le propriétaire de l’objet.

</dd> <dt>

<span id="group_sid"></span><span id="GROUP_SID"></span>sid du groupe \_
</dt> <dd>

Chaîne SID qui identifie le groupe principal de l’objet.

</dd> <dt>

<span id="dacl_flags"></span><span id="DACL_FLAGS"></span>\_indicateurs DACL
</dt> <dd>

Indicateurs de contrôle du descripteur de sécurité qui s’appliquent à la liste DACL. Pour obtenir une description de ces indicateurs de contrôle, consultez la fonction [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) . La \_ chaîne d’indicateurs DACL peut être une concaténation de zéro ou plusieurs des chaînes suivantes.



| Contrôler               | Constante dans SDDL. h       | Signification                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| P                   | SDDL \_ protégé          | L' \_ indicateur de \_ protection discrétionnaire se est défini.          |
| AR                  | \_demande d' \_ héritage \_ automatique SDDL | L’indicateur de demande d’héritage automatique de la liste d’accès \_ discrétionnaire \_ \_ \_ est défini. |
| AI                  | SDDL \_ \_ hérité automatiquement    | L' \_ indicateur d’héritage automatique de la liste de \_ \_ rédépendance se définit.    |
| « AUCUN \_ contrôle d’accès \_ » | ACL de la \_ valeur null SSDL \_          | La liste de contrôle d’accès a la valeur null.                              |



 

</dd> <dt>

<span id="sacl_flags"></span><span id="SACL_FLAGS"></span>\_indicateurs SACL
</dt> <dd>

Indicateurs de contrôle du descripteur de sécurité qui s’appliquent à la liste SACL. La \_ chaîne d’indicateurs SACL utilise les mêmes chaînes de bits de contrôle que la \_ chaîne d’indicateurs DACL.

</dd> <dt>

<span id="string_ace"></span><span id="STRING_ACE"></span>chaîne \_ ACE
</dt> <dd>

Chaîne qui décrit une entrée du contrôle d’accès dans la liste DACL ou SACL du descripteur de sécurité. Pour obtenir une description du format de chaîne ACE, consultez [chaînes ACE](ace-strings.md). Chaque chaîne ACE est placée entre parenthèses (()).

</dd> </dl>

Les composants inutiles peuvent être omis de la chaîne de descripteur de sécurité. Par exemple, si l' \_ \_ indicateur de présence DACL se n’est pas défini dans le descripteur de sécurité d’entrée, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) n’inclut pas de composant D : dans la chaîne de sortie. Vous pouvez également utiliser les indicateurs de bits des [**\_ informations de sécurité**](security-information.md) pour indiquer les composants à inclure dans une chaîne de descripteur de sécurité.

Le format de chaîne de descripteur de sécurité ne prend pas en charge les ACL **null** .

Pour désigner une liste de contrôle d’accès vide, la chaîne de descripteur de sécurité comprend le jeton D : ou S : sans informations de chaîne supplémentaires.

La chaîne de descripteur de sécurité stocke les bits de [**contrôle de DEscripteur de sécurité**](security-descriptor-control.md) de différentes façons. Les éléments \_ de la liste de réédition DACL se présentent \_ par la \_ \_ présence du jeton D : ou S : dans la chaîne. Les autres bits qui s’appliquent à la liste DACL ou SACL sont stockés dans les \_ indicateurs DACL et les \_ indicateurs SACL. Le propriétaire SE est \_ \_ par défaut, le groupe de se par défaut, le \_ \_ \_ DACL de se \_ par défaut et les \_ bits SACL par défaut de se ne \_ sont pas stockés dans une chaîne de descripteur de sécurité. Le \_ bit Auto \_ relatif de se n’est pas stocké dans la chaîne, mais [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) définit toujours ce bit dans le descripteur de sécurité de sortie.

Les exemples suivants montrent des chaînes de descripteur de sécurité et les informations contenues dans les descripteurs de sécurité associés.

Chaîne 1 :


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



Descripteur de sécurité 1 :


```C++
    Revision:  0x00000001
    Control:   0x0004
        SE_DACL_PRESENT
    Owner: (S-1-5-32-548)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x02
    Size:     0x001c
    AceCount: 0x0001
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x100e003f
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            GENERIC_ALL
                            Others(0x0000003f)
        Ace Sid      : (S-1-0-0)
SACL
    Not present
```



Chaîne 2 :


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



Descripteur de sécurité 2 :


```C++
    Revision:  0x00000001
    Control:   0x0014
        SE_DACL_PRESENT
        SE_SACL_PRESENT
    Owner: (S-1-5-21-397955417-626881126-188441444-512)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x04
    Size:     0x0104
    AceCount: 0x0007
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-18)
    Ace[01]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0024
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-21-397955417-626881126-188441444-512)
    Ace[02]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_USER
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[03]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_GROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[04]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_LOCALGROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[05]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_PRINT_QUEUE
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-550)
    Ace[06]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x00020014
                            READ_CONTROL
                            Others(0x00000014)
        Ace Sid:       (S-1-5-11)
    SACL
        Revision: 0x02
        Size:     0x001c
        AceCount: 0x0001
        Ace[00]
            AceType:       0x02 (SYSTEM_AUDIT_ACE_TYPE)
            AceSize:       0x0014
            InheritFlags:  0xc0
                SUCCESSFUL_ACCESS_ACE_FLAG
                FAILED_ACCESS_ACE_FLAG
            Access Mask:    0x000d002b
                                DELETE
                                WRITE_DAC
                                WRITE_OWNER
                                Others(0x0000002b)
            Ace Sid:       (S-1-1-0)
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Chaînes ACE](ace-strings.md)
</dt> <dt>

[Langage de définition du descripteur de sécurité pour les ACE conditionnelles](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
