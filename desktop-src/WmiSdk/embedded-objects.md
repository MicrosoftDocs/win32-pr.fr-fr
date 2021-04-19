---
description: Un objet incorporé est un objet d’une classe qui existe dans une déclaration de classe ou d’instance d’une autre classe.
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: Incorporation d’objets dans une classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518821"
---
# <a name="embedding-objects-in-a-class"></a>Incorporation d’objets dans une classe

Un objet incorporé est un objet d’une classe qui existe dans une déclaration de classe ou d’instance d’une autre classe. Par exemple, la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) contient des objets incorporés [**Win32 \_ Trusted**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) . Chacun des objets **de \_ confiance Win32** contient un [**objet \_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) . WMI ne limite pas la profondeur à laquelle une classe peut avoir des objets incorporés. Toutefois, l’utilisation d’une autre conception, telle que la création d’une classe d’association, peut rendre un schéma plus gérable.

Pour plus d’informations sur les objets incorporés, consultez les rubriques suivantes :

-   [Création d’objets incorporés](creating-embedded-objects.md)
-   [Interrogation d’objets incorporés](querying-embedded-objects.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
