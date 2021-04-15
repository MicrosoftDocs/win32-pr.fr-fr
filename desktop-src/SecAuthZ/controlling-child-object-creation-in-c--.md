---
description: Vous pouvez utiliser la liste DACL d’un objet conteneur pour contrôler qui est autorisé à créer des objets enfants dans le conteneur.
ms.assetid: 95f2f058-f847-4f58-b469-090bf599ae98
title: Contrôle de la création d’objets enfants en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598b2fd9a9889fbb77d2b3a4ecd004efcd823b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527639"
---
# <a name="controlling-child-object-creation-in-c"></a><span data-ttu-id="81e38-103">Contrôle de la création d’objets enfants en C++</span><span class="sxs-lookup"><span data-stu-id="81e38-103">Controlling Child Object Creation in C++</span></span>

<span data-ttu-id="81e38-104">Vous pouvez utiliser la liste DACL d’un objet conteneur pour contrôler qui est autorisé à créer des objets enfants dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="81e38-104">You can use the DACL of a container object to control who is allowed to create child objects within the container.</span></span> <span data-ttu-id="81e38-105">Cela peut être important, car le créateur d’un objet est généralement affecté en tant que propriétaire de l’objet, et le propriétaire d’un objet peut contrôler l’accès à l’objet.</span><span class="sxs-lookup"><span data-stu-id="81e38-105">This can be important because the creator of an object is typically assigned as the object's owner, and an object's owner can control access to the object.</span></span>

<span data-ttu-id="81e38-106">Les différents types d’objets conteneur possèdent des droits d’accès spécifiques qui contrôlent la possibilité de créer des objets enfants.</span><span class="sxs-lookup"><span data-stu-id="81e38-106">The various types of container objects have specific access rights that control the ability to create child objects.</span></span> <span data-ttu-id="81e38-107">Par exemple, un thread doit avoir un \_ accès clé créer une \_ sous \_ -clé à une clé de Registre pour créer une sous-clé sous la clé.</span><span class="sxs-lookup"><span data-stu-id="81e38-107">For example, a thread must have KEY\_CREATE\_SUB\_KEY access to a registry key to create a subkey under the key.</span></span> <span data-ttu-id="81e38-108">La liste DACL d’une clé de Registre peut contenir des ACE qui autorisent ou refusent ce droit d’accès.</span><span class="sxs-lookup"><span data-stu-id="81e38-108">The DACL of a registry key can contain ACEs that allow or deny this access right.</span></span> <span data-ttu-id="81e38-109">De même, NTFS prend en charge les droits d’accès fichier ajouter un fichier \_ \_ et fichier \_ ajouter \_ un sous-répertoire pour contrôler la possibilité de créer des fichiers ou des répertoires dans un répertoire.</span><span class="sxs-lookup"><span data-stu-id="81e38-109">Similarly, NTFS supports the FILE\_ADD\_FILE and FILE\_ADD\_SUBDIRECTORY access rights for controlling the ability to create files or directories in a directory.</span></span>

<span data-ttu-id="81e38-110">Le droit ad \_ droit \_ créer un \_ \_ accès enfant contrôle la création d’objets enfants dans un objet de service d’annuaire (DS).</span><span class="sxs-lookup"><span data-stu-id="81e38-110">The ADS\_RIGHT\_DS\_CREATE\_CHILD access right controls the creation of child objects in a directory service (DS) object.</span></span> <span data-ttu-id="81e38-111">Toutefois, les objets DS peuvent contenir différents types d’objets, de sorte que le système prend en charge une granularité plus fine.</span><span class="sxs-lookup"><span data-stu-id="81e38-111">However, DS objects can contain different types of objects, so the system supports a finer granularity of control.</span></span> <span data-ttu-id="81e38-112">Vous pouvez utiliser des [ACE spécifiques](object-specific-aces.md) à un objet pour autoriser ou refuser le droit de créer un type spécifié d’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="81e38-112">You can use [object-specific ACEs](object-specific-aces.md) to allow or deny the right to create a specified type of child object.</span></span> <span data-ttu-id="81e38-113">Vous pouvez autoriser un utilisateur à créer un type d’objet enfant tout en empêchant l’utilisateur de créer d’autres types d’objets enfants.</span><span class="sxs-lookup"><span data-stu-id="81e38-113">You can allow a user to create one type of child object while preventing the user from creating other types of child objects.</span></span>

<span data-ttu-id="81e38-114">L’exemple suivant utilise la fonction [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) pour ajouter une entrée du contrôle d’accès spécifique à un objet à une liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="81e38-114">The following example uses the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to add an object-specific ACE to an ACL.</span></span> <span data-ttu-id="81e38-115">L’ACE accorde l’autorisation de créer un type spécifié d’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="81e38-115">The ACE grants permission to create a specified type of child object.</span></span> <span data-ttu-id="81e38-116">Le membre **grfAccessPermissions** de la structure d' [**\_ accès explicite**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) est défini sur ADS \_ droit créer un \_ \_ \_ enfant pour indiquer que l’ACE contrôle la création de l’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="81e38-116">The **grfAccessPermissions** member of the [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structure is set to ADS\_RIGHT\_DS\_CREATE\_CHILD to indicate that the ACE controls the child object creation.</span></span> <span data-ttu-id="81e38-117">Le membre **ObjectsPresent** de la structure [**Objects \_ and \_ sid**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) a la valeur \_ type d’objet ACE \_ \_ présent pour indiquer que le membre **ObjectTypeGuid** contient un GUID valide.</span><span class="sxs-lookup"><span data-stu-id="81e38-117">The **ObjectsPresent** member of the [**OBJECTS\_AND\_SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) structure is set to ACE\_OBJECT\_TYPE\_PRESENT to indicate that the **ObjectTypeGuid** member contains a valid GUID.</span></span> <span data-ttu-id="81e38-118">Le GUID identifie un type d’objet enfant dont la création est contrôlée.</span><span class="sxs-lookup"><span data-stu-id="81e38-118">The GUID identifies a type of child object whose creation is being controlled.</span></span>

<span data-ttu-id="81e38-119">Dans l’exemple suivant, pOldDACL doit être un pointeur valide vers une structure [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) existante.</span><span class="sxs-lookup"><span data-stu-id="81e38-119">In the following example, pOldDACL must be a valid pointer to an existing [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) structure.</span></span> <span data-ttu-id="81e38-120">Pour plus d’informations sur la création d’une structure **ACL** pour un objet, consultez [création d’un descripteur de sécurité pour un nouvel objet en C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="81e38-120">For information about how to create an **ACL** structure for an object, see [Creating a Security Descriptor for a New Object in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span></span>


```C++
DWORD dwRes;
PACL pOldDACL = NULL;
PACL pNewDACL = NULL;
GUID guidChildObjectType = GUID_NULL;   // GUID of object to control creation of
PSID pTrusteeSID = NULL;           // trustee for new ACE
EXPLICIT_ACCESS ea;
OBJECTS_AND_SID ObjectsAndSID;

// pOldDACL must be a valid pointer to an existing ACL structure.

// guidChildObjectType must be the GUID of an object type 
// that is a possible child of the object associated with pOldDACL.
 
// Initialize an OBJECTS_AND_SID structure with object type GUIDs and 
// the SID of the trustee for the new ACE. 

ZeroMemory(&ObjectsAndSID, sizeof(OBJECTS_AND_SID));
ObjectsAndSID.ObjectsPresent = ACE_OBJECT_TYPE_PRESENT;
ObjectsAndSID.ObjectTypeGuid = guidChildObjectType;
ObjectsAndSID.InheritedObjectTypeGuid  = GUID_NULL;
ObjectsAndSID.pSid = (SID *)pTrusteeSID;

// Initialize an EXPLICIT_ACCESS structure for the new ACE. 

ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
ea.grfAccessPermissions = ADS_RIGHT_DS_CREATE_CHILD;
ea.grfAccessMode = GRANT_ACCESS;
ea.grfInheritance= NO_INHERITANCE;
ea.Trustee.TrusteeForm = TRUSTEE_IS_OBJECTS_AND_SID;
ea.Trustee.ptstrName = (LPTSTR) &ObjectsAndSID;

// Create a new ACL that merges the new ACE
// into the existing DACL.

dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
```



 

 



