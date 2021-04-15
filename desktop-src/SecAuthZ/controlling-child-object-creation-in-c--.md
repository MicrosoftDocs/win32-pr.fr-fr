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
# <a name="controlling-child-object-creation-in-c"></a>Contrôle de la création d’objets enfants en C++

Vous pouvez utiliser la liste DACL d’un objet conteneur pour contrôler qui est autorisé à créer des objets enfants dans le conteneur. Cela peut être important, car le créateur d’un objet est généralement affecté en tant que propriétaire de l’objet, et le propriétaire d’un objet peut contrôler l’accès à l’objet.

Les différents types d’objets conteneur possèdent des droits d’accès spécifiques qui contrôlent la possibilité de créer des objets enfants. Par exemple, un thread doit avoir un \_ accès clé créer une \_ sous \_ -clé à une clé de Registre pour créer une sous-clé sous la clé. La liste DACL d’une clé de Registre peut contenir des ACE qui autorisent ou refusent ce droit d’accès. De même, NTFS prend en charge les droits d’accès fichier ajouter un fichier \_ \_ et fichier \_ ajouter \_ un sous-répertoire pour contrôler la possibilité de créer des fichiers ou des répertoires dans un répertoire.

Le droit ad \_ droit \_ créer un \_ \_ accès enfant contrôle la création d’objets enfants dans un objet de service d’annuaire (DS). Toutefois, les objets DS peuvent contenir différents types d’objets, de sorte que le système prend en charge une granularité plus fine. Vous pouvez utiliser des [ACE spécifiques](object-specific-aces.md) à un objet pour autoriser ou refuser le droit de créer un type spécifié d’objet enfant. Vous pouvez autoriser un utilisateur à créer un type d’objet enfant tout en empêchant l’utilisateur de créer d’autres types d’objets enfants.

L’exemple suivant utilise la fonction [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) pour ajouter une entrée du contrôle d’accès spécifique à un objet à une liste de contrôle d’accès. L’ACE accorde l’autorisation de créer un type spécifié d’objet enfant. Le membre **grfAccessPermissions** de la structure d' [**\_ accès explicite**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) est défini sur ADS \_ droit créer un \_ \_ \_ enfant pour indiquer que l’ACE contrôle la création de l’objet enfant. Le membre **ObjectsPresent** de la structure [**Objects \_ and \_ sid**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) a la valeur \_ type d’objet ACE \_ \_ présent pour indiquer que le membre **ObjectTypeGuid** contient un GUID valide. Le GUID identifie un type d’objet enfant dont la création est contrôlée.

Dans l’exemple suivant, pOldDACL doit être un pointeur valide vers une structure [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) existante. Pour plus d’informations sur la création d’une structure **ACL** pour un objet, consultez [création d’un descripteur de sécurité pour un nouvel objet en C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).


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



 

 



