---
description: Le \_ NetworkLoginProfile Win32&\# 8194 ; La classe WMI représente les informations de connexion réseau d’un utilisateur spécifique sur un système informatique exécutant Windows.
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Classe Win32_NetworkLoginProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4fb71b27093cb1011b9aebaadf0a6760124b64f9e13ae7b5ef46f5ffc478cce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972648"
---
# <a name="win32_networkloginprofile-class"></a>\_Classe NetworkLoginProfile Win32

La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkLoginProfile** WMI représente les informations de connexion réseau d’un utilisateur spécifique sur un système informatique exécutant Windows. Cela comprend, mais ne se limite pas à l’état du mot de passe, les privilèges d’accès, les quotas de disque et les chemins d’accès aux répertoires de connexion.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ NetworkLoginProfile** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ NetworkLoginProfile** a ces propriétés.

<dl> <dt>

**AccountExpires dans**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ compte \_ expire »)
</dt> </dl>

Le compte va expirer. Cette valeur est calculée à partir du nombre de secondes écoulées depuis le 00:00:00, le 1er janvier 1970, et est défini au format suivant : AAAAMMJJHHMMSS. mmmmmm sutc.

Exemple : 20521201000230,000000 000

</dd> <dt>

**AuthorizationFlags**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ auth \_ Flags »), [**bitvalues**](../wmisdk/standard-qualifiers.md) (« Printer », « communication », « Server », « Accounts »)
</dt> </dl>

Ensemble d’indicateurs qui spécifient les ressources qu’un utilisateur est autorisé à utiliser ou modifier.

<dt>

1 (0x1)
</dt> <dd>

Imprimante

</dd> <dt>

2 (0X2)
</dt> <dd>

Communication

</dd> <dt>

4 (0x4)
</dt> <dd>

Serveur

</dd> <dt>

8 (0x8)
</dt> <dd>

Comptes

</dd> </dl>

</dd> <dt>

**BadPasswordCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management Functions \| NetUserEnum »)
</dt> </dl>

Nombre de fois où l’utilisateur entre un mot de passe incorrect lors de la connexion à un système informatique exécutant Windows.

Exemple : 0

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Courte description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**CodePage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 page de \_ codes \_ »)
</dt> </dl>

Page de codes pour le langage de votre choix. Une page de codes est le jeu de caractères utilisé.

</dd> <dt>

**Commentaire**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Comment »)
</dt> </dl>

Commentaire ou description pour ce profil d’ouverture de session.

</dd> <dt>

**CountryCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Country \_ Code »)
</dt> </dl>

Code de pays/région pour la langue choisie par l’utilisateur.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**Indicateurs**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags »), [**bitmap**](../wmisdk/standard-qualifiers.md) (« 0 », « 1 "," 3 "," 4 "," 5 "," 6 "," 7 "," 8 "," 9 "," 11 "," 12 "," 13 "," 16 "," 17 "," 18 "," 19 "," 20 "," 21 "," 22 "," 23 "), [**BitValue**](../wmisdk/standard-qualifiers.md) (" script "," compte désactivé "," répertoire de départ requis "," verrouillage "," mot de passe non requis "," Paswword ne peut pas changer "," mot de passe de test chiffré autorisé "," compte Temp dupliqué "," compte normal "," compte de confiance interdomaine ", «compte d’approbation de station de travail », « compte de confiance de serveur », « ne pas faire expirer le mot de passe », « compte d’ouverture de session MNS », « carte à puce requise », « approuvé pour la délégation », « non délégué », « utiliser la clé des uniquement », « ne pas exiger une pré-autorisation »
</dt> </dl>

Propriétés disponibles pour ce profil réseau.

Les propriétés qui peuvent être définies sont les suivantes :

<dt>

1 (0x1)
</dt> <dd>

Script

Un script d’ouverture de session exécuté. Cette valeur doit être définie pour LAN Manager 2,0.

</dd> <dt>

2 (0X2)
</dt> <dd>

Compte désactivé

Le compte de l’utilisateur est désactivé.

</dd> <dt>

8 (0x8)
</dt> <dd>

Répertoire de démarrage requis

Un répertoire de départ est requis.

</dd> <dt>

16 (0x10)
</dt> <dd>

Verrouillage.

Le compte est actuellement verrouillé. Pour [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), cette valeur peut être désactivée pour déverrouiller un compte précédemment verrouillé. Cette valeur ne peut pas être utilisée pour verrouiller un compte précédemment déverrouillé.

</dd> <dt>

32 (0x20)
</dt> <dd>

Mot de passe non requis

Aucun mot de passe n'est requis.

</dd> <dt>

64 (0x40)
</dt> <dd>

Le mot de passe ne peut pas être modifié

L’utilisateur ne peut pas modifier le mot de passe.

</dd> <dt>

128 (0x80)
</dt> <dd>

Mot de passe de test chiffré autorisé

</dd> <dt>

256 (0x100)
</dt> <dd>

Compte temporaire dupliqué

Compte pour les utilisateurs dont le compte principal se trouve dans un autre domaine. Ce compte fournit l’accès utilisateur à ce domaine, mais pas à un domaine qui approuve ce domaine. Le gestionnaire de l’utilisateur fait référence à ce type de compte en tant que compte d’utilisateur local.

</dd> <dt>

512 (0x200)
</dt> <dd>

Compte normal

Type de compte par défaut qui représente un utilisateur standard.

</dd> <dt>

2048 (0x800)
</dt> <dd>

Compte de confiance interdomaine

Autorisation à un compte de confiance pour un domaine qui approuve d’autres domaines.

</dd> <dt>

4096 (0x1000)
</dt> <dd>

Compte d’approbation de station de travail

un compte d’ordinateur pour un Windows station de travail ou un serveur qui est membre de ce domaine.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

Compte de confiance du serveur

Un compte d’ordinateur pour un contrôleur de domaine de sauvegarde qui est membre de ce domaine.

</dd> <dt>

65536 (0x10000)
</dt> <dd>

Ne pas faire expirer le mot de passe

</dd> <dt>

131072 (0x20000)
</dt> <dd>

Compte d’ouverture de session MNS

Type de compte d’ouverture de session jeu de nœud majoritaire (MNS) qui représente un utilisateur MNS.

</dd> <dt>

262144 (0x40000)
</dt> <dd>

Carte à puce requise

</dd> <dt>

524288 (0x80000)
</dt> <dd>

Approuvé pour la délégation

</dd> <dt>

1048576 ()
</dt> <dd>

Non délégué

</dd> <dt>

2097152 (0x200000)
</dt> <dd>

Utiliser la clé DES uniquement

</dd> <dt>

4194304 (0x400000)
</dt> <dd>

Ne pas exiger la pré-autorisation

</dd> <dt>

8388608 (0x800000)
</dt> <dd>

Mot de passe expiré

Indique que le mot de passe a expiré.

</dd> </dl>

Les propriétés suivantes décrivent le type de compte. Une seule valeur peut être définie :

-   \_compte standard \_ uf
-   \_ \_ compte DUPLIQUÉ temporaire \_ uf
-   compte d’approbation de station de \_ travail UF \_ \_
-   \_compte de \_ confiance du serveur uf \_
-   \_compte de confiance interdomaine UF \_ \_

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Full \_ Name »)
</dt> </dl>

Nom complet de l’utilisateur appartenant au profil de connexion réseau. Cette chaîne peut être vide si l’utilisateur choisit de ne pas associer un nom complet à un nom d’utilisateur.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ orig \_ dir »)
</dt> </dl>

Chemin d’accès au répertoire de départ de l’utilisateur. Cette chaîne peut être vide si l’utilisateur choisit de ne pas spécifier de répertoire de démarrage.

Exemple : « \\ homedir »

</dd> <dt>

**HomeDirectoryDrive**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ orig \_ dir \_ Drive »)
</dt> </dl>

Lettre de lecteur affectée au répertoire de démarrage de l’utilisateur pour la connexion.

Exemple : "C :"

</dd> <dt>

**LastLogoff**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Last \_ Logoff »)
</dt> </dl>

Dernière déconnexion du système par l’utilisateur. Cette valeur est calculée à partir du nombre de secondes écoulées depuis le 00:00:00, le 1er janvier 1970. La valeur « \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* » signifie que l’heure de la dernière déconnexion est inconnue. Le format de cette valeur est AAAAMMJJHHMMSS. mmmmmm sutc. Pour plus d’informations sur la traduction de cette propriété en heure locale, consultez [tâches WMI : dates et heures](../wmisdk/wmi-tasks--dates-and-times.md).

Exemple : 19521201000230,000000 000

</dd> <dt>

**LastLogon**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Last \_ Logon »)
</dt> </dl>

Dernier utilisateur ayant ouvert une session sur le système. Cette valeur est calculée à partir du nombre de secondes écoulées depuis le 00:00:00, le 1er janvier 1970. Le format de cette valeur est AAAAMMJJHHMMSS. mmmmmm sutc. Pour plus d’informations sur la traduction de cette propriété en heure locale, consultez [tâches WMI : dates et heures](../wmisdk/wmi-tasks--dates-and-times.md).

Exemple : 19521201000230,000000 000

</dd> <dt>

**LogonHours**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ hours")
</dt> </dl>

Heures de la semaine auxquelles l’utilisateur peut se connecter. Chaque bit représente une unité de temps spécifiée par la propriété **UnitsPerWeek** . Par exemple, si l’unité de temps est horaire, le premier bit (bit 0, mot 0) est dimanche, 0:00 à 0:59, le deuxième bit (bit 1, mot 0) est dimanche, 1:00 à 1:59, et ainsi de suite. Si ce membre a la valeur **null**, il n’y a aucune restriction de temps. L’heure est définie sur GMT et doit être ajustée pour les autres fuseaux horaires (par exemple, GMT moins 8 heures pour PST).

</dd> <dt>

**LogonServer**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ Server »)
</dt> </dl>

Nom du serveur auquel les demandes d’ouverture de session sont envoyées. Les noms de serveur doivent être précédés de deux barres obliques inverses ( \\ \\ ). Un nom de serveur avec un astérisque ( \\ \\ \* ) indique que la demande d’ouverture de session peut être gérée par n’importe quel serveur d’ouverture de session. Une chaîne NULL indique que les demandes sont envoyées au contrôleur de domaine.

Exemple : « \\ \\ MyServer »

</dd> <dt>

**MaximumStorage**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api des \| structures de gestion de réseau \| [**\_ \_**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Max \_ Storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantité maximale d’espace disque disponible pour l’utilisateur. Si MaximumStorage est défini sur USER \_ MAXSTORAGE \_ Unlimited, l’utilisateur est autorisé à utiliser tout l’espace disque disponible.

Exemple : 10 millions

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Name")
</dt> </dl>

Compte d’utilisateur sur un domaine ou un ordinateur particulier. Le nombre de caractères dans le nom ne peut pas dépasser la valeur de UNLEN.

Exemple : « somedomain \\ JohnDoe »

</dd> <dt>

**NumberOfLogons**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ num \_ Logons »)
</dt> </dl>

Nombre de fois où l’utilisateur a réussi à se connecter à ce compte. La valeur 0xFFFFFFFF indique que la valeur est inconnue. Cette propriété est conservée séparément sur chaque contrôleur de domaine de sauvegarde (BDC) du domaine. Pour avoir une valeur précise, seule la plus grande valeur de tous les contrôleurs secondaires de domaine doit être utilisée.

Example: 4

</dd> <dt>

**Paramètres**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ parms »)
</dt> </dl>

Espace réservé pour une utilisation par les applications. Cette chaîne peut avoir la valeur null, ou elle peut avoir n’importe quel nombre de caractères avant le caractère null de fin. Les produits Microsoft utilisent ce membre pour stocker les informations de configuration de l’utilisateur. Ne modifiez pas ces informations, car cette valeur est spécifique à une application.

</dd> <dt>

**Mot de passe**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ password \_ Age »)
</dt> </dl>

Durée pendant laquelle un mot de passe a été appliqué. Cette valeur est mesurée à partir du nombre de secondes écoulées depuis la dernière modification du mot de passe.

Exemple : 00001201000230,000000 000

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**User \_ modals \_ info \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ Max \_ passwd passwd \_ Age »)
</dt> </dl>

Date et heure d’expiration du mot de passe. La valeur est définie dans le format suivant : AAAAMMJJHHMMSS. mmmmmm sutc

Exemple : 19521201000230,000000 000

</dd> <dt>

**PrimaryGroupId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 ID de \_ \_ groupe principal \_ »)
</dt> </dl>

Identificateur relatif (RID) du groupe global principal de cet utilisateur. L’identificateur vérifie le groupe principal auquel appartient le profil de l’utilisateur.

</dd> <dt>

**Privilèges**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ priv »)
</dt> </dl>

Niveau de privilège affecté à la propriété de **\_ nom usri3** .

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

**Invité** (0)


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

**Utilisateur** (1)


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

**Administrateur** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Profil**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ »)
</dt> </dl>

Chemin d’accès au profil de l’utilisateur. Cette valeur peut être une chaîne NULL, un chemin d’accès absolu local ou un chemin d’accès UNC. Un profil utilisateur contient des paramètres qui peuvent être personnalisés pour chaque utilisateur, tels que les couleurs du bureau.

Exemple : « C : \\ Windows »

</dd> <dt>

**ScriptPath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ script \_ Path »)
</dt> </dl>

Chemin d’accès du répertoire du script d’ouverture de session de l’utilisateur. Un script d’ouverture de session exécute automatiquement un ensemble de commandes chaque fois qu’un utilisateur se connecte à un système.

Exemple : « C : \\ Win \\ Profiles \\ ThomasSteven »

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificateur par lequel l’objet actuel est connu.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**UnitsPerWeek**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Units \_ per \_ week »)
</dt> </dl>

Nombre d’unités de temps où la semaine est divisée. Elle est utilisée avec la propriété **LogonHours** pour limiter l’accès utilisateur à l’ordinateur.

Exemple : 168 (heures par semaine)

</dd> <dt>

**UserComment**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ Comment »)
</dt> </dl>

Commentaire ou description défini par l’utilisateur pour ce profil.

</dd> <dt>

**UserId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ User \_ ID »)
</dt> </dl>

RID de l’utilisateur. L’identificateur vérifie que l’utilisateur existe et qu’il est unique à ce domaine.

</dd> <dt>

**UserType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags »)
</dt> </dl>

Type de compte auquel l’utilisateur a des privilèges.

Les valeurs sont :

-   « Compte normal »
-   « Compte dupliqué »
-   « Compte d’approbation de station de travail »
-   « Compte de confiance de serveur »
-   « Compte de confiance interdomaine »
-   Connue

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

**Compte normal** (« compte normal »)


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

**Compte en double** (« compte dupliqué »)


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

**Compte de confiance de station de travail** (« compte d’approbation de station de travail »)


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

**Compte de confiance de serveur** (« compte de confiance de serveur »)


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

**Compte de confiance interdomaine** (« compte de confiance interdomaine »)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** ("inconnu")


</dt> <dd></dd> </dl>

</dd> <dt>

**Stations**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 stations de \_ travail »)
</dt> </dl>

Noms des postes de travail à partir desquels l’utilisateur peut ouvrir une session. Vous pouvez spécifier jusqu’à huit stations de travail ; les noms doivent être séparés par des virgules (,). Une chaîne NULL indique qu’il n’y A aucune restriction. Pour désactiver les ouvertures de session de toutes les stations de travail de ce compte, définissez la valeur UF \_ ACCOUNTDISABLE dans la propriété **Flags** de cette classe.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ NetworkLoginProfile** est dérivée [**du \_ paramètre CIM**](cim-setting.md).

le processus appelant qui utilise cette classe doit avoir le privilège **SE \_ restore \_ NAME** sur l’ordinateur où se trouve le registre. Pour plus d’informations, consultez [exécution d’opérations privilégiées](../wmisdk/executing-privileged-operations.md).

## <a name="examples"></a>Exemples

L’exemple PowerShell [List login Network Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) retourne les informations de connexion réseau pour tous les utilisateurs d’un ordinateur.

L’exemple VBScript suivant retourne les informations de connexion réseau.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
```



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
