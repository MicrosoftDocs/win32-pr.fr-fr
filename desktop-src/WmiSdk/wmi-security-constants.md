---
description: WMI vérifie les droits d’accès pour les applications et les scripts.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Constantes de sécurité WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2f3a8ff4727852637fe6e4b808f0b8d3a74c958808cb3beb7bc9df32b0c995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739416"
---
# <a name="wmi-security-constants"></a>Constantes de sécurité WMI

WMI vérifie les droits d’accès pour les applications et les scripts pour des objets tels que les espaces de noms WMI, les imprimantes, les services, les applications DCOM, les fichiers, les partages et d’autres objets sécurisables. L’accès à ces objets sécurisables est contrôlé par les entrées de contrôle d’accès (ACE). Chaque ACE contient des listes qui désignent les groupes ou utilisateurs qui ont accès. Pour plus d’informations sur la sécurité et les listes de contrôle d’accès (ACL, DACL ou SACL), consultez [listes de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists) et [descripteurs de sécurité](/windows/desktop/SecAuthZ/security-descriptors).

De nombreuses méthodes de fournisseur dans WMI qui affectent des objets sécurisables requièrent que l’administrateur Active certains privilèges. La version du privilège que vous utilisez dépend du langage de programmation, comme indiqué dans [**constantes de privilège**](privilege-constants.md).

Les constantes de sécurité sont définies dans les rubriques suivantes :

-   [**Constantes de sécurité d’événement**](event-security-constants.md)
-   [**Constantes de droits d’accès aux fichiers et aux répertoires**](file-and-directory-access-rights-constants.md)
-   [**Constantes de droits d’accès à l’espace de noms**](namespace-access-rights-constants.md)
-   [**Constantes d’indicateur ACE d’espace de noms**](namespace-ace-flag-constants.md)
-   [**Constantes de type d’ACE d’espace de noms**](namespace-ace-type-constants.md)
-   [**Constantes de privilège**](privilege-constants.md)

 

 
