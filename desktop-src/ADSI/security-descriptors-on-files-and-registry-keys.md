---
title: Descripteurs de sécurité sur les fichiers et les clés de Registre
description: Les interfaces ADSI (Active Directory Service Interfaces) peuvent être utilisées pour gérer et sécuriser les systèmes de fichiers au sein d’une organisation, y compris la possibilité de définir ou de modifier des ACL sur des fichiers ou des partages de fichiers créés par des utilisateurs.
ms.assetid: 7233a82f-fc38-4718-b674-4e6a00666184
ms.tgt_platform: multiple
keywords:
- Descripteurs de sécurité sur les fichiers et les clés de Registre ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11600a495b9a70513b9bd401777e9cdd61449ede
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463707"
---
# <a name="security-descriptors-on-files-and-registry-keys"></a><span data-ttu-id="a1386-104">Descripteurs de sécurité sur les fichiers et les clés de Registre</span><span class="sxs-lookup"><span data-stu-id="a1386-104">Security Descriptors on Files and Registry Keys</span></span>

<span data-ttu-id="a1386-105">Les interfaces ADSI (Active Directory Service Interfaces) peuvent être utilisées pour gérer et sécuriser les systèmes de fichiers au sein d’une organisation, y compris la possibilité de définir ou de modifier des ACL sur des fichiers ou des partages de fichiers créés par des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a1386-105">Active Directory Service Interfaces (ADSI) can be used to manage and secure file systems within an organization, including the ability to set or modify ACLs on files or file shares created by users.</span></span> <span data-ttu-id="a1386-106">Les interfaces de sécurité, telles que [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)et [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , définissent des ACL sur Active Directory, Exchange, un fichier, un partage de fichiers ou des objets de clé de registre.</span><span class="sxs-lookup"><span data-stu-id="a1386-106">Security interfaces, such as [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) set ACLs on Active Directory, Exchange, file, file share, or registry key objects.</span></span> <span data-ttu-id="a1386-107">Avant d’utiliser ces interfaces, vous devrez peut-être modifier le descripteur de sécurité s’il utilise un format différent de celui de l’interface ou si vous n’avez pas de droits d’accès à la liste SACL du descripteur de sécurité, car vous n’êtes pas membre du groupe administrateurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a1386-107">Before using these interfaces, the security descriptor may need to be modified if it uses a different format from the interface, or if you do not have access rights to the SACL of the security descriptor because you are not a member of the security administrator group.</span></span>

<span data-ttu-id="a1386-108">Pour récupérer, définir ou modifier le descripteur de sécurité, utilisez l’interface [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) .</span><span class="sxs-lookup"><span data-stu-id="a1386-108">To get, set, or modify the security descriptor, use the [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) interface.</span></span> <span data-ttu-id="a1386-109">Cette interface vous permet de récupérer un descripteur de sécurité à partir de différentes ressources dans son format d’origine (par exemple, le format ADSI [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), un descripteur de sécurité brut ou une chaîne hexadécimale utilisée dans Exchange 5,5).</span><span class="sxs-lookup"><span data-stu-id="a1386-109">This interface enables you to retrieve a security descriptor from various resources in its original format, such as the ADSI format [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), a raw security descriptor, or as a hexadecimal string as used in Exchange 5.5.</span></span> <span data-ttu-id="a1386-110">Une fois récupéré, vous pouvez le convertir dans un autre format, par exemple à partir d’un descripteur de sécurité brut vers **IADsSecurityDescriptor**.</span><span class="sxs-lookup"><span data-stu-id="a1386-110">When retrieved, you can convert it to another format, for example, from a raw security descriptor to **IADsSecurityDescriptor**.</span></span> <span data-ttu-id="a1386-111">Vous pouvez ensuite réécrire le nouveau format dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="a1386-111">You can then write the new format back to the resource.</span></span>

<span data-ttu-id="a1386-112">Certaines des valeurs de propriété [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , telles que [**AccessMask**](iadsaccesscontrolentry-property-methods.md) et **AceFlags**, sont différentes pour différents types d’objets.</span><span class="sxs-lookup"><span data-stu-id="a1386-112">Some of the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) property values, such as [**AccessMask**](iadsaccesscontrolentry-property-methods.md) and **AceFlags**, will be different for different object types.</span></span> <span data-ttu-id="a1386-113">Par exemple, un objet Active Directory utilise le membre **de \_ \_ \_ lecture générique droit ADS** de l’énumération d’énumération des [**\_ droits \_ ADS**](/windows/win32/api/iads/ne-iads-ads_rights_enum) pour la propriété **IADsAccessControlEntry. AccessMask** , mais le droit d’accès équivalent pour un objet fichier est **\_ \_ lecture générique de fichier**.</span><span class="sxs-lookup"><span data-stu-id="a1386-113">For example, an Active Directory object will use the **ADS\_RIGHT\_GENERIC\_READ** member of the [**ADS\_RIGHTS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) enumeration for the **IADsAccessControlEntry.AccessMask** property, but the equivalent access right for a file object is **FILE\_GENERIC\_READ**.</span></span> <span data-ttu-id="a1386-114">Il n’est pas possible de supposer que toutes les valeurs de propriété seront les mêmes pour les objets Active Directory et les objets non Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a1386-114">It is not safe to assume that all property values will be the same for Active Directory objects and non-Active Directory objects.</span></span> <span data-ttu-id="a1386-115">La liste suivante répertorie les propriétés **IADsAccessControlEntry** qui diffèrent pour les objets non-Active Directory et où les valeurs appropriées peuvent être obtenues.</span><span class="sxs-lookup"><span data-stu-id="a1386-115">The following list shows the **IADsAccessControlEntry** properties that differ for non-Active Directory objects and where the proper values can be obtained.</span></span>

<dl> <dt>

<span data-ttu-id="a1386-116"><span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="a1386-116"><span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="a1386-117">Pour plus d’informations et pour obtenir la liste des valeurs possibles pour les objets fichier ou partage de fichiers, consultez [sécurité des fichiers et droits d’accès](/windows/desktop/FileIO/file-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="a1386-117">For more information and a list of possible values for file or file share objects, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights).</span></span>

<span data-ttu-id="a1386-118">Pour plus d’informations et pour obtenir la liste des valeurs possibles pour les objets du Registre, consultez [sécurité des clés de Registre et droits d’accès](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="a1386-118">For more information and a list of possible values for registry objects, see [Registry Key Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span></span>

</dd> <dt>

<span data-ttu-id="a1386-119"><span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="a1386-119"><span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="a1386-120">Pour plus d’informations, consultez le membre **AceType** de la structure d' [**\_ en-tête ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="a1386-120">For more information, see the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a1386-121"><span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="a1386-121"><span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="a1386-122">Pour plus d’informations, consultez le membre **AceFlags** de la structure d' [**\_ en-tête ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="a1386-122">For more information, see the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a1386-123"><span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Père**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="a1386-123"><span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Flags**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="a1386-124">Contient zéro ou une combinaison d’une ou plusieurs des valeurs suivantes de Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="a1386-124">Contains zero or a combination of one or more of the following values from WinNT.h.</span></span>

<dl> <dt>

<span data-ttu-id="a1386-125"><span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE \_ TYPE d’objet \_ \_ présent** (1)</span><span class="sxs-lookup"><span data-stu-id="a1386-125"><span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE\_OBJECT\_TYPE\_PRESENT** (1)</span></span>
</dt> <dd>

<span data-ttu-id="a1386-126">[**ObjectType**](iadsaccesscontrolentry-property-methods.md) contient une valeur valide.</span><span class="sxs-lookup"><span data-stu-id="a1386-126">[**ObjectType**](iadsaccesscontrolentry-property-methods.md) contains a valid value.</span></span>

</dd> <dt>

<span data-ttu-id="a1386-127"><span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE \_ \_Type d’objet hérité \_ \_ présent** (2)</span><span class="sxs-lookup"><span data-stu-id="a1386-127"><span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE\_INHERITED\_OBJECT\_TYPE\_PRESENT** (2)</span></span>
</dt> <dd>

<span data-ttu-id="a1386-128">[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) contient une valeur valide.</span><span class="sxs-lookup"><span data-stu-id="a1386-128">[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) contains a valid value.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a1386-129"><span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="a1386-129"><span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="a1386-130">Pour plus d’informations, consultez le membre **ObjectType** de [**l' \_ ACE Access denied \_ Object \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**Access \_ allowed \_ Object \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)et des structures similaires.</span><span class="sxs-lookup"><span data-stu-id="a1386-130">For more information, see the **ObjectType** member of the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace), and similar structures.</span></span> <span data-ttu-id="a1386-131">Cette propriété ne doit pas être définie ou modifiée pour des objets non-Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a1386-131">This property should not be set or modified for non-Active Directory objects.</span></span>

</dd> <dt>

<span data-ttu-id="a1386-132"><span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="a1386-132"><span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="a1386-133">Pour plus d’informations, consultez le membre **InheritedObjectType** de [**l' \_ \_ \_ ACE Access denied Object**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**Access \_ allowed \_ Object \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)et des structures similaires.</span><span class="sxs-lookup"><span data-stu-id="a1386-133">For more information, see the **InheritedObjectType** member of the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace), and similar structures.</span></span> <span data-ttu-id="a1386-134">Cette propriété ne doit pas être définie ou modifiée pour des objets non-Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a1386-134">This property should not be set or modified for non-Active Directory objects.</span></span>

</dd> </dl>

<span data-ttu-id="a1386-135">Normalement, [**IADsSecurityUtility. GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) récupère toutes les parties du descripteur de sécurité, telles que Owner, Group, SACL ou DACL.</span><span class="sxs-lookup"><span data-stu-id="a1386-135">Normally, [**IADsSecurityUtility.GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) will retrieve all parts of the security descriptor, such as owner, group, SACL, or DACL.</span></span> <span data-ttu-id="a1386-136">De même, [**IADsSecurityUtility. SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) remplace toutes les parties du descripteur de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="a1386-136">Similarly, [**IADsSecurityUtility.SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) will overwrite all parts of the security descriptor by default.</span></span> <span data-ttu-id="a1386-137">Vous pouvez utiliser la propriété [**IADsSecurityUtility. SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) pour spécifier des parties individuelles du descripteur de sécurité à récupérer ou à définir.</span><span class="sxs-lookup"><span data-stu-id="a1386-137">You can use the [**IADsSecurityUtility.SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) property to specify individual parts of the security descriptor to retrieve or set.</span></span> <span data-ttu-id="a1386-138">Par exemple, vous pouvez définir **SecurityMask** sur [**ADS \_ Security \_ info \_ DACL**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) avant d’appeler **GetSecurityDescriptor** pour récupérer uniquement la liste DACL sans récupérer les autres parties du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a1386-138">For example, you can set **SecurityMask** to [**ADS\_SECURITY\_INFO\_DACL**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) before calling **GetSecurityDescriptor** to only retrieve the DACL without retrieving the other parts of the security descriptor.</span></span>

<span data-ttu-id="a1386-139">Pour plus d’informations et pour obtenir un exemple de code qui utilise l’interface [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) pour ajouter une entrée du contrôle d’accès à un fichier, consultez l' [exemple de code pour l’ajout](example-code-for-adding-an-ace-to-a-file.md)d’une entrée du contrôle d’accès à un fichier.</span><span class="sxs-lookup"><span data-stu-id="a1386-139">For more information and a code example that uses the [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) interface to add an ACE to a file, see [Example Code for Adding an ACE to a File](example-code-for-adding-an-ace-to-a-file.md).</span></span>

<span data-ttu-id="a1386-140">L’exemple de code suivant fournit les identificateurs constants pour les propriétés de fichier, de partage de fichiers et de Registre pour les propriétés [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags** et **Flags** à utiliser avec Visual Basic et Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="a1386-140">The following example code provides the constant identifiers for file, file share and registry objects for the [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags**, and **Flags** properties for use with Visual Basic and Microsoft Visual Basic Scripting Edition.</span></span>


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



 

 