---
title: Descripteurs de sécurité sur les fichiers et les clés de Registre
description: Les interfaces ADSI (Active Directory Service Interfaces) peuvent être utilisées pour gérer et sécuriser les systèmes de fichiers au sein d’une organisation, y compris la possibilité de définir ou de modifier des ACL sur des fichiers ou des partages de fichiers créés par des utilisateurs.
ms.assetid: 7233a82f-fc38-4718-b674-4e6a00666184
ms.tgt_platform: multiple
keywords:
- Descripteurs de sécurité sur les fichiers et les clés de Registre ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae567e9550989153f0b85207be49a729bc0499c320f410c92fc993269d997da7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333219"
---
# <a name="security-descriptors-on-files-and-registry-keys"></a>Descripteurs de sécurité sur les fichiers et les clés de Registre

Les interfaces ADSI (Active Directory Service Interfaces) peuvent être utilisées pour gérer et sécuriser les systèmes de fichiers au sein d’une organisation, y compris la possibilité de définir ou de modifier des ACL sur des fichiers ou des partages de fichiers créés par des utilisateurs. les interfaces de sécurité, telles que [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)et [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , définissent des acl sur Active Directory, Exchange, un fichier, un partage de fichiers ou des objets de clé de registre. Avant d’utiliser ces interfaces, vous devrez peut-être modifier le descripteur de sécurité s’il utilise un format différent de celui de l’interface ou si vous n’avez pas de droits d’accès à la liste SACL du descripteur de sécurité, car vous n’êtes pas membre du groupe administrateurs de sécurité.

Pour récupérer, définir ou modifier le descripteur de sécurité, utilisez l’interface [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) . cette interface vous permet de récupérer un descripteur de sécurité à partir de différentes ressources dans son format d’origine (par exemple, le format ADSI [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), un descripteur de sécurité brut ou une chaîne hexadécimale utilisée dans Exchange 5,5). Une fois récupéré, vous pouvez le convertir dans un autre format, par exemple à partir d’un descripteur de sécurité brut vers **IADsSecurityDescriptor**. Vous pouvez ensuite réécrire le nouveau format dans la ressource.

Certaines des valeurs de propriété [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , telles que [**AccessMask**](iadsaccesscontrolentry-property-methods.md) et **AceFlags**, sont différentes pour différents types d’objets. Par exemple, un objet Active Directory utilise le membre **de \_ \_ \_ lecture générique droit ADS** de l’énumération d’énumération des [**\_ droits \_ ADS**](/windows/win32/api/iads/ne-iads-ads_rights_enum) pour la propriété **IADsAccessControlEntry. AccessMask** , mais le droit d’accès équivalent pour un objet fichier est **\_ \_ lecture générique de fichier**. Il n’est pas possible de supposer que toutes les valeurs de propriété seront les mêmes pour les objets Active Directory et les objets non Active Directory. La liste suivante répertorie les propriétés **IADsAccessControlEntry** qui diffèrent pour les objets non-Active Directory et où les valeurs appropriées peuvent être obtenues.

<dl> <dt>

<span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Pour plus d’informations et pour obtenir la liste des valeurs possibles pour les objets fichier ou partage de fichiers, consultez [sécurité des fichiers et droits d’accès](/windows/desktop/FileIO/file-security-and-access-rights).

Pour plus d’informations et pour obtenir la liste des valeurs possibles pour les objets du Registre, consultez [sécurité des clés de Registre et droits d’accès](/windows/desktop/SysInfo/registry-key-security-and-access-rights).

</dd> <dt>

<span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Pour plus d’informations, consultez le membre **AceType** de la structure d' [**\_ en-tête ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .

</dd> <dt>

<span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Pour plus d’informations, consultez le membre **AceFlags** de la structure d' [**\_ en-tête ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .

</dd> <dt>

<span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Père**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Contient zéro ou une combinaison d’une ou plusieurs des valeurs suivantes de Winnt. h.

<dl> <dt>

<span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE \_ TYPE d’objet \_ \_ présent** (1)
</dt> <dd>

[**ObjectType**](iadsaccesscontrolentry-property-methods.md) contient une valeur valide.

</dd> <dt>

<span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE \_ \_Type d’objet hérité \_ \_ présent** (2)
</dt> <dd>

[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) contient une valeur valide.

</dd> </dl> </dd> <dt>

<span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Pour plus d’informations, consultez le membre **ObjectType** de [**l' \_ ACE Access denied \_ Object \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**Access \_ allowed \_ Object \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)et des structures similaires. Cette propriété ne doit pas être définie ou modifiée pour des objets non-Active Directory.

</dd> <dt>

<span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Pour plus d’informations, consultez le membre **InheritedObjectType** de [**l' \_ \_ \_ ACE Access denied Object**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**Access \_ allowed \_ Object \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)et des structures similaires. Cette propriété ne doit pas être définie ou modifiée pour des objets non-Active Directory.

</dd> </dl>

Normalement, [**IADsSecurityUtility. GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) récupère toutes les parties du descripteur de sécurité, telles que Owner, Group, SACL ou DACL. De même, [**IADsSecurityUtility. SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) remplace toutes les parties du descripteur de sécurité par défaut. Vous pouvez utiliser la propriété [**IADsSecurityUtility. SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) pour spécifier des parties individuelles du descripteur de sécurité à récupérer ou à définir. Par exemple, vous pouvez définir **SecurityMask** sur [**ADS \_ Security \_ info \_ DACL**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) avant d’appeler **GetSecurityDescriptor** pour récupérer uniquement la liste DACL sans récupérer les autres parties du descripteur de sécurité.

Pour plus d’informations et pour obtenir un exemple de code qui utilise l’interface [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) pour ajouter une entrée du contrôle d’accès à un fichier, consultez l' [exemple de code pour l’ajout](example-code-for-adding-an-ace-to-a-file.md)d’une entrée du contrôle d’accès à un fichier.

l’exemple de code suivant fournit les identificateurs constants pour les propriétés de fichier, de partage de fichiers et de registre pour les propriétés [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags** et **flags** à utiliser avec Visual Basic et Microsoft Visual Basic scripting Edition.


```VB
' Identifiers for the IADsAccessControlEntry.AccessMask property for file,
' file share, and registry objects.
Const DELETE = &H10000
Const READ_CONTROL = &H20000
Const WRITE_DAC = &H40000
Const WRITE_OWNER = &H80000
Const SYNCHRONIZE = &H100000

Const STANDARD_RIGHTS_REQUIRED = &HF0000

Const STANDARD_RIGHTS_READ = &H20000
Const STANDARD_RIGHTS_WRITE = &H20000
Const STANDARD_RIGHTS_EXECUTE = &H20000

Const STANDARD_RIGHTS_ALL = &H1F0000

Const SPECIFIC_RIGHTS_ALL = &HFFFF

' Identifiers for the IADsAccessControlEntry.AccessMask property for file and
' file share objects.
Const FILE_READ_DATA = &H1                  '  file & pipe
Const FILE_LIST_DIRECTORY = &H1             '  directory

Const FILE_WRITE_DATA = &H2                 '  file & pipe
Const FILE_ADD_FILE = &H2                   '  directory

Const FILE_APPEND_DATA = &H4                '  file
Const FILE_ADD_SUBDIRECTORY = &H4           '  directory
Const FILE_CREATE_PIPE_INSTANCE = &H4       '  named pipe

Const FILE_READ_EA = &H8                    '  file & directory

Const FILE_WRITE_EA = &H10                  '  file & directory

Const FILE_EXECUTE = &H20                   '  file
Const FILE_TRAVERSE = &H20                  '  directory

Const FILE_DELETE_CHILD = &H40              '  directory

Const FILE_READ_ATTRIBUTES = &H80           '  all

Const FILE_WRITE_ATTRIBUTES = &H100         '  all

Const FILE_ALL_ACCESS = STANDARD_RIGHTS_REQUIRED Or SYNCHRONIZE Or &H1FF

Const FILE_GENERIC_READ = STANDARD_RIGHTS_READ Or FILE_READ_DATA Or FILE_READ_ATTRIBUTES Or _
                          FILE_READ_EA Or SYNCHRONIZE

Const FILE_GENERIC_WRITE = STANDARD_RIGHTS_WRITE Or FILE_WRITE_DATA Or FILE_WRITE_ATTRIBUTES Or _
                           FILE_WRITE_EA Or FILE_APPEND_DATA Or SYNCHRONIZE

Const FILE_GENERIC_EXECUTE = STANDARD_RIGHTS_EXECUTE Or FILE_READ_ATTRIBUTES Or FILE_EXECUTE Or SYNCHRONIZE


' Identifiers for the IADsAccessControlEntry.AccessMask property for registry
' objects.
Const KEY_QUERY_VALUE = &H1
Const KEY_SET_VALUE = &H2
Const KEY_CREATE_SUB_KEY = &H4
Const KEY_ENUMERATE_SUB_KEYS = &H8
Const KEY_NOTIFY = &H10
Const KEY_CREATE_LINK = &H20
Const KEY_WOW64_32KEY = &H200
Const KEY_WOW64_64KEY = &H100
Const KEY_WOW64_RES = &H300

Const KEY_READ = ((STANDARD_RIGHTS_READ Or KEY_QUERY_VALUE Or KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY) And _
                  (Not SYNCHRONIZE))

Const KEY_WRITE = ((STANDARD_RIGHTS_WRITE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY) And (Not SYNCHRONIZE))

Const KEY_EXECUTE = ((KEY_READ) And (Not SYNCHRONIZE))

Const KEY_ALL_ACCESS = ((STANDARD_RIGHTS_ALL Or KEY_QUERY_VALUE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY Or _
                         KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY Or KEY_CREATE_LINK) And (Not SYNCHRONIZE))
    

' Identifiers for the IADsAccessControlEntry.AceFlags property for file and
' file share objects.
Const OBJECT_INHERIT_ACE = &H1
Const CONTAINER_INHERIT_ACE = &H2
Const NO_PROPAGATE_INHERIT_ACE = &H4
Const INHERIT_ONLY_ACE = &H8
Const INHERITED_ACE = &H10
    

' Identifiers for the IADsAccessControlEntry.Flags property.
Const ACE_OBJECT_TYPE_PRESENT = 1
Const ACE_INHERITED_OBJECT_TYPE_PRESENT = 2
```



 

 