---
description: Le modèle de sécurité Windows vous permet de contrôler l’accès aux objets de mappage de fichiers. Pour plus d’informations, consultez Access-Control modèle.
ms.assetid: 8bbf7c98-ff83-4ed9-8b82-f08dcd31295c
title: Sécurité du mappage de fichiers et droits d’accès
ms.topic: article
ms.date: 10/06/2018
ms.openlocfilehash: 65d520e12d1b555e7c633f0d1e0ba5142c330ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515221"
---
# <a name="file-mapping-security-and-access-rights"></a>Sécurité du mappage de fichiers et droits d’accès

Le modèle de sécurité Windows vous permet de contrôler l’accès aux objets de mappage de fichiers. Pour plus d’informations, consultez [modèle de contrôle d’accès](../secauthz/access-control-model.md).

Vous pouvez spécifier un [descripteur de sécurité](../secauthz/security-descriptors.md) pour un objet de mappage de fichiers lorsque vous appelez la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) . Si vous spécifiez **null**, l’objet obtient un descripteur de sécurité par défaut. Les listes de contrôle d’accès dans le descripteur de sécurité par défaut pour un objet de mappage de fichiers proviennent du jeton principal ou d’emprunt d’identité du créateur.

Pour récupérer le descripteur de sécurité d’un objet de mappage de fichier, appelez la fonction [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo) . Pour définir le descripteur de sécurité d’un objet de mappage de fichier, appelez la fonction [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa) ou [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

Les droits d’accès valides pour les objets de mappage de fichiers incluent les [droits d’accès](../secauthz/standard-access-rights.md)de **suppression**, de **\_ contrôle de lecture**, d' **écriture \_ DAC** et de **\_ propriétaire d’écriture** . Les objets de mappage de fichiers ne prennent pas en charge le droit d’accès **synchronisation** standard. Le tableau suivant répertorie les droits d’accès spécifiques aux objets de mappage de fichiers.

| Droit d’accès | Signification |
|-|-|
| **Explorateur de fichiers- \_ \_ tous les \_ accès** | Comprend tous les droits d’accès à un objet de mappage de fichiers à l’exception de l' **\_ \_ exécution de mappages de fichiers**. Les fonctions [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) et [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) traitent cela comme la spécification de l' **\_ \_ écriture de mappage de fichier**. |
| **mappage de fichiers \_ \_ exécuté** | Autorise le mappage des vues exécutables de l’objet de mappage de fichier. L’objet doit avoir été créé avec la protection de page qui autorise l’accès en exécution, par exemple **page \_ Execute \_ Read**, **page \_ Execute \_ WRITECOPY** ou **page \_ Execute \_ ReadWrite** protection.  |
| **\_lecture de mappage de fichier \_** | Autorise le mappage des vues en lecture seule ou de copie sur écriture de l’objet de mappage de fichier.  |
| **\_écriture de mappage de fichier \_** | Permet le mappage des vues en lecture seule, de copie sur écriture ou de lecture/écriture d’un objet de mappage de fichier. L’objet doit avoir été créé avec la protection de page qui autorise l’accès en écriture, par exemple **page \_ ReadWrite** ou **page \_ Execute \_ ReadWrite** protection. |

Le mappage d’une vue de copie en écriture d’un objet de mappage de fichiers requiert le même accès que le mappage d’une vue en lecture seule. L’indicateur de **\_ \_ copie de mappage de fichier** n’est pas un droit d’accès et ne doit pas être spécifié dans le cadre d’une liste DACL dans un descripteur de sécurité. Cette valeur peut être utilisée uniquement avec les fonctions qui mappent une vue d’un objet de mappage de fichiers, comme les fonctions [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) et [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) , ou avec la fonction [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) , qui traite la **copie de \_ mappage \_ de fichier** de la même façon qu’elle traite la **lecture de \_ mappage \_ de fichier**.

Vous pouvez demander le droit accès à la **\_ \_ sécurité du système d’accès** à un objet de mappage de fichiers si vous souhaitez lire ou écrire la liste SACL de l’objet. Pour plus d’informations, consultez [listes de contrôle d’accès (ACL)](../secauthz/access-control-lists.md) et [droit d’accès SACL](../secauthz/sacl-access-right.md).
