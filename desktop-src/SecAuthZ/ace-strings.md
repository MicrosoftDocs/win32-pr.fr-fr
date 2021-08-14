---
description: Explique les chaînes utilisées dans une entrée de contrôle d’accès.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: Chaînes ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60e8f4f5d3cd94f6e871b3b4962d2d548afa003c3bd4aa37a1ae8f008ce1a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785400"
---
# <a name="ace-strings"></a>Chaînes ACE

Le [langage SDDL (Security Descriptor Definition Language](security-descriptor-definition-language.md) ) utilise des chaînes ACE dans les composants DACL et SACL d’une chaîne de [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) .

Comme indiqué dans les exemples de [format de chaîne de descripteur de sécurité](security-descriptor-string-format.md) , chaque entrée du contrôle d’accès dans une chaîne de descripteur de sécurité est placée entre parenthèses. Les champs de l’entrée du contrôle d’accès sont dans l’ordre suivant et sont séparés par des points-virgules (;).

> [!Note]  
> Il existe un format différent pour les [*entrées du contrôle d’accès*](/windows/desktop/SecGloss/a-gly) conditionnel (ACE) par rapport aux autres types ACE. Pour les ACE conditionnelles, consultez [langage de définition du descripteur de sécurité pour les ACE conditionnelles](security-descriptor-definition-language-for-conditional-aces-.md).

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a>Champs

<dl> <dt>

<span id="ace_type"></span><span id="ACE_TYPE"></span>**type d’entrée de contrôle d’accès \_**
</dt> <dd>

Chaîne qui indique la valeur du membre **AceType** de la structure d' [**\_ en-tête ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . La chaîne de type ACE peut être l’une des chaînes suivantes définies dans SDDL. h.



| Chaîne de type ACE | Constante dans SDDL. h                      | Valeur AceType                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| « A »             | \_accès SDDL \_ autorisé                   | TYPE d’entrée du contrôle d’accès \_ autorisé \_ \_                                                                                                                                         |
| « D »             | \_accès SDDL \_ refusé                    | TYPE d’entrée du contrôle d’accès \_ refusé \_ \_                                                                                                                                          |
| FONCTIONNEMENT            | \_ \_ accès à l’objet SDDL \_ autorisé           | \_type d' \_ ACE d’objet autorisé \_ d’accès \_                                                                                                                                 |
| DIAMÈTRE            | \_ \_ accès à l’objet SDDL \_ refusé            | \_type d' \_ ACE d’objet accès refusé \_ \_                                                                                                                                  |
| UA            | \_audit SDDL                             | \_type d' \_ entrée du contrôle d’accès système \_                                                                                                                                           |
| "AL"            | \_alarme SDDL                             | \_type d' \_ ACE d’alarme système \_                                                                                                                                           |
| Organisation            | \_audit des objets SDDL \_                     | \_type d' \_ ACE d’objet d’audit système \_ \_                                                                                                                                   |
| OL            | \_alarme d’objet SDDL \_                     | \_type d' \_ ACE d’objet d’alarme système \_ \_                                                                                                                                   |
| « ML »            | étiquette de SDDL \_ obligatoire \_                  | \_TYPE d’ACE du LABEL obligatoire du système \_ \_ \_ **Windows serveur 2003 :** non disponible.                                                                                        |
| XA            | \_ \_ accès au rappel SDDL \_ autorisé         | accès \_ autorisé \_ au \_ TYPE de l’ACE de rappel \_ **Windows serveur 2008, Windows Vista et Windows server 2003 :** non disponible.                                                |
| VERROUILLAGE            | \_ \_ accès au rappel SDDL \_ refusé          | \_TYPE d’ACE de rappel de refus d’accès \_ \_ \_ **Windows serveur 2008, Windows Vista et Windows server 2003 :** non disponible.                                                 |
| INSCRIPTION            | \_attribut de ressource SDDL \_               | \_attribut de ressource système \_ \_ ACE \_ TYPE **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista et Windows server 2003 :** non disponible.<br/> |
| SR            | ID de stratégie de l' \_ étendue SDDL \_ \_                | \_ \_ TYPE d’ACE de l’ID de stratégie système \_ \_ \_ **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista et Windows server 2003 :** non disponible.<br/>  |
| "XU"            | \_audit de rappel SDDL \_                   | \_TYPE d’entrée de contrôle d’accès de rappel du système \_ \_ \_ **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista et Windows server 2003 :** non disponible.<br/>     |
| ARMÉNIENNE            | \_ \_ accès à l’objet de rappel SDDL \_ \_ autorisé | TYPE d’entrée du contrôle d’accès autorisé pour le \_ \_ rappel \_ \_ **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista et Windows server 2003 :** non disponible.<br/>   |
| TL            | \_étiquette d' \_ approbation de processus SDDL \_             | \_TYPE d' \_ entrée de contrôle d’accès de l’étiquette d’approbation du processus système \_ \_ \_ **Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista et Windows Server 2003 :** non disponible. |
| TX            | \_filtre d’accès SDDL \_                    | \_TYPE d’ACE du filtre d’accès système \_ \_ \_ **Windows Server 2016, Windows 10 version 1607, Windows 10 version 1511, Windows 10 version 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista et Windows server 2003 :** non disponible. |
 

> [!Note]  
> Si le type d' **entrée \_** du contrôle d’accès est \_ \_ \_ \_ un type d’ACE d’objet autorisé d’accès [](/windows/win32/api/guiddef/ns-guiddef-guid) et que le GUID d’objet n’est pas spécifié pour le GUID de l’objet, [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) convertit le **\_ type d’entrée** du contrôle d’accès en type ACE **\_ \_** **\_** \_ autorisé \_ \_ .

 

</dd> <dt>

<span id="ace_flags"></span><span id="ACE_FLAGS"></span>**\_indicateurs ACE**
</dt> <dd>

Chaîne qui indique la valeur du membre **AceFlags** de la structure d' [**\_ en-tête ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . La chaîne d’indicateurs ACE peut être une concaténation des chaînes suivantes définies dans SDDL. h.



| Chaîne des indicateurs ACE | Constante dans SDDL. h       | Valeur AceFlag                 |
|------------------|--------------------------|-------------------------------|
| CI             | \_hériter du conteneur SDDL \_ | \_ACE d’héritage de conteneur \_       |
| OI             | l' \_ objet SDDL \_ hérite    | l’objet \_ hérite de l' \_ ACE          |
| ENTRANT             | SDDL \_ non \_ propagé      | AUCUNE \_ propagation d' \_ entrée de contrôle d’accès \_   |
| ENTRÉES             | SDDL \_ hérite \_ uniquement      | HÉRITer \_ uniquement \_ ACE            |
| « ID »             | SDDL \_ hérité          | \_ACE hérité                |
| SA             | \_réussite de l’audit SDDL \_     | \_ \_ indicateur ACE d’accès réussi \_ |
| Param             | \_échec de l’audit SDDL \_     | \_ \_ indicateur ACE d’accès en échec \_     |
| PM             | \_ \_ filtre protégé d’approbation SDDL \_ | \_indicateur ACE du filtre protégé par approbation \_ \_ \_ **Windows Server 2016, Windows 10 version 1607, Windows 10 version 1511, Windows 10 version 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista et Windows server 2003 :** non disponible. |
| CR             | SDDL \_ critique           | \_indicateur ACE \_ critique **Windows server version 1803, Windows 10 version 1803, Windows server version 1709, Windows 10 version 1709, Windows 10 version 1703, Windows Server 2016, Windows 10 version 1607, Windows 10 version 1511, Windows 10 version 1507, Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008, Windows Vista et Windows Server 2003 :** non disponible. |
 

</dd> <dt>

<span id="rights"></span><span id="RIGHTS"></span>**autorisations**
</dt> <dd>

Chaîne qui indique les [droits d’accès](access-rights-and-access-masks.md) contrôlés par l’entrée du contrôle d’accès. Cette chaîne peut être une représentation sous forme de chaîne hexadécimale des droits d’accès, par exemple « 0x7800003F », ou il peut s’agir d’une concaténation des chaînes suivantes.



### <a name="generic-access-rights"></a>Droits d’accès génériques

| Chaîne de droits d’accès | Constante dans SDDL. h | Valeur du droit d’accès |
|----------------------|--------------------|--------------------|
| DISPONIBLE                 | SDDL \_ générique \_ tout | GÉNÉRIQUE \_ tout       |
| EM                 | \_lecture générique \_ SDDL | \_lecture générique     |
| ENTREPÔT                 | \_écriture générique \_ SDDL | \_écriture générique |
| GX                 | \_Exécution générique \_ SDDL | \_Exécution générique |


### <a name="standard-access-rights"></a>Droits d’accès standard

| Chaîne de droits d’accès | Constante dans SDDL. h | Valeur du droit d’accès |
|----------------------|--------------------|--------------------|
| Release                 | \_contrôle de lecture SDDL \_ | LIRE \_ le contrôle      |
| DP                 | \_suppression standard \_ SDDL | Suppression          |
| WD                 | \_écriture DAC d’écriture SDDL \_ | ÉCRITURE \_ DAC            |
| WO                 | \_propriétaire d’écriture SDDL \_ | propriétaire en écriture \_        |

### <a name="directory-service-object-access-rights"></a>Droits d’accès à l’objet service d’annuaire

| Chaîne de droits d’accès | Constante dans SDDL. h | Valeur du droit d’accès |
|----------------------|--------------------|--------------------|
| PR                 | \_propriété de lecture SDDL \_ | \_lecture de \_ la \_ \_ prop DS droite des publicités |
| EP                 | \_propriété d’écriture SDDL \_ | \_Prop. \_ d' \_ écriture DS droit \_ ads |
| CC                 | SDDL- \_ créer un \_ enfant | création d’un enfant ad \_ Right \_ DS \_ \_ |
| MÉTAFICHIER                 | \_enfant de suppression SDDL \_ | \_enfant ad droit \_ supprimer un \_ \_ enfant |
| EUROS                 | enfants de la \_ liste SDDL \_ | \_liste des \_ ACTRL \_ DS \_ pour les publicités |
| EPP                 | écriture SDDL en \_ \_ écriture    | active \_ Directory avec droit ad \_ \_ |
| Lo                  | \_objet de liste SDDL \_ | \_objet de \_ \_ liste DS Right ad \_ |
| DIV                 | \_arborescence de suppression SDDL \_ | \_arborescence de \_ suppression du service d’annuaire AD Right \_ \_ |
| CR                  | \_ \_ accès au contrôle SDDL | \_ \_ \_ accès au contrôle du service d’annuaire AD Right \_ |

### <a name="file-access-rights"></a>Droits d’accès au fichier

| Chaîne de droits d’accès | Constante dans SDDL. h | Valeur du droit d’accès |
|----------------------|--------------------|--------------------|
| Param                 | \_fichier SDDL \_ tout    | FICHIER \_ tout \_ accès   |
| FR                 | \_lecture du fichier SDDL \_   | \_lecture générique du fichier \_ |
| PARE                 | \_écriture de fichier SDDL \_  | \_écriture générique du fichier \_ |
| ROTATION                 | \_exécution du fichier SDDL \_ | FICHIER \_ générique \_ exécuter |


### <a name="registry-key-access-rights"></a>Droits d’accès à la clé de Registre

| Chaîne de droits d’accès | Constante dans SDDL. h | Valeur du droit d’accès |
|----------------------|--------------------|--------------------|
| Ka                 | \_clé SDDL \_ tout     | \_tout \_ accéder à la clé   |
| Corée                 | lecture de la \_ clé SDDL \_    | lecture de la clé \_          |
| KWh                 | écriture de la \_ clé SDDL \_   | écriture de clé \_         |
| "KX"                 | \_clé SDDL \_ exécutée | exécution de la clé \_       |

### <a name="mandatory-label-rights"></a>Droits d’étiquette obligatoires

| Chaîne de droits d’accès | Constante dans SDDL. h | Valeur du droit d’accès |
|----------------------|--------------------|--------------------|
| Nr                 | SDDL \_ non \_ lu \_ | \_étiquette obligatoire \_ système \_ non \_ en \_ lecture **Windows serveur 2008, Windows Vista et Windows server 2003 :** non disponible. |
| 11LE                 | SDDL \_ non \_ écrit \_ | \_étiquette obligatoire \_ système \_ non \_ \_ en écriture **Windows serveur 2008, Windows Vista et Windows server 2003 :** non disponible. |
| NX                 | SDDL \_ non \_ exécuté \_ | \_étiquette obligatoire \_ système \_ non \_ exécutée \_ **Windows serveur 2008, Windows Vista et Windows server 2003 :** non disponible. |
</dd> <dt>

<span id="object_guid"></span><span id="OBJECT_GUID"></span>**GUID de l’objet \_**
</dt> <dd>

Représentation sous forme de chaîne d’un GUID qui indique la valeur du membre **ObjectType** d’une structure d’entrée du contrôle d’accès spécifique à l’objet, telle que l' [**\_ ACE access allowed \_ Object \_**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace). La chaîne GUID utilise le format retourné par la fonction [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .

Le tableau suivant répertorie certains GUID d’objets couramment utilisés.



| Droits et GUID                         | Autorisation      |
|-----------------------------------------|-----------------|
| CR ; ab721a53-1e2f-11D0-9819-00aa0040529b | Modifier le mot de passe |
| CR ; 00299570-246d-11D0-A768-00aa006e0529 | Réinitialiser le mot de passe  |



 

</dd> <dt>

<span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**hériter du \_ GUID d’objet \_**
</dt> <dd>

Représentation sous forme de chaîne d’un GUID qui indique la valeur du membre **InheritedObjectType** d’une structure ACE spécifique à un objet. La chaîne GUID utilise le format [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .

</dd> <dt>

<span id="account_sid"></span><span id="ACCOUNT_SID"></span>**sid du compte \_**
</dt> <dd>

[Chaîne sid](sid-strings.md) qui identifie le [tiers de confiance](trustees.md) de l’entrée du contrôle d’accès.

</dd> <dt>

<span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**attribut de ressource \_**
</dt> <dd>

\[FACULTATIF \] l' \_ attribut de ressource est uniquement destiné aux ACE de ressource et est facultatif. Chaîne qui indique le type de données. Le type de données de l’ACE de l’attribut de ressource peut être l’un des types de données suivants définis dans SDDL. h.

Le \# signe « » est synonyme de «0 » dans les attributs de ressource. Par exemple, D :AI (XA ; OICI ; FA ;;; WD ; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) est équivalent à et interprété comme D :ai (XA ; oici ; FA ;;; WD ; (OctetStringType = = \# 01020300)).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista et Windows server 2003 :** Les attributs de ressource ne sont pas disponibles.



| Chaîne de type de données ACE attribut de ressource | Constante dans SDDL. h | Type de données        |
|-----------------------------------------|--------------------|------------------|
| ÉC                                    | SDDL \_ int          | Entier signé   |
| PÉTAL                                    | SDDL \_ uint         | Entier non signé |
| TS                                    | \_WSTRING SDDL      | Chaîne étendue      |
| ÉQUIPEMENTS                                    | \_sid SDDL          | SID              |
| ÉMETTEUR                                    | \_objet BLOB SDDL         | Chaîne d’octets     |
| TO                                    | SDDL \_ booléen      | Boolean          |



 

</dd> </dl>

L’exemple suivant illustre une chaîne ACE pour une entrée du contrôle d’accès autorisée. Comme il ne s’agit pas d’une entrée du contrôle d’accès spécifique à un objet, elle ne contient pas d’informations dans les champs **\_ GUID d’objet** et **hériter du \_ \_ GUID d’objet** . Le **champ \_ indicateurs ACE** est également vide, ce qui indique qu’aucun des indicateurs ACE n’est défini.


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



La chaîne ACE présentée ci-dessus décrit les informations ACE suivantes.


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



l’exemple suivant montre un fichier classé avec des revendications de ressource pour Windows et langage SQL (SQL) avec un secret défini sur un Impact professionnel élevé.


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



La chaîne ACE présentée ci-dessus décrit les informations ACE suivantes.


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



Pour plus d’informations, consultez [format de chaîne du descripteur de sécurité](security-descriptor-string-format.md) et [chaînes sid](sid-strings.md). Pour les ACE conditionnelles, consultez [langage de définition du descripteur de sécurité pour les ACE conditionnelles](security-descriptor-definition-language-for-conditional-aces-.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[\[MS-DTYP \] : langage de description du descripteur de sécurité](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

