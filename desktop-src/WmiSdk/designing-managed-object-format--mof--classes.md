---
description: Un fournisseur WMI se compose d’un fichier de format MOF (MOF) et d’un fichier DLL. Le fichier MOF définit les classes pour lesquelles l’implémentation du fournisseur fournit des données.
ms.assetid: 20ef6b88-2aaa-4e86-bc4a-bebc34069672
ms.tgt_platform: multiple
title: Conception de classes format MOF (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 201f8c45f7a247fbca5695baa6dd440fc5dc323f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203739"
---
# <a name="designing-managed-object-format-mof-classes"></a>Conception de classes format MOF (MOF)

Un [*fournisseur WMI*](gloss-p.md) se compose d’un fichier de format MOF (MOF) et d’un fichier dll. Le fichier MOF définit les classes pour lesquelles l’implémentation du fournisseur fournit des données.

Les définitions de classe MOF sont compilées par l’utilitaire [**mofcomp**](mofcomp.md) et stockées dans le [*référentiel WMI*](gloss-w.md), également connu sous le nom de référentiel Common Information Model (CIM). Une façon moins courante de créer des classes consiste à utiliser les méthodes de l' [API com pour WMI](com-api-for-wmi.md).

> [!Note]  
> Pour vous assurer que toutes les définitions de classe WMI pour les objets managés sont restaurées dans l' [*espace de stockage WMI*](gloss-w.md) en cas d’échec et de redémarrage de WMI, utilisez l’instruction [**\# pragma AutoRecover**](pragma-autorecover.md) de préprocesseur dans votre fichier MOF.

 

Les sections suivantes sont présentées dans cette rubrique :

-   [Définition des objets à gérer](#defining-the-objects-to-manage)
-   [Définition des propriétés ou des méthodes](#defining-properties-or-methods)
-   [Association d’objets entre eux](#relating-objects-to-each-other)
-   [Rubriques connexes](#related-topics)

## <a name="defining-the-objects-to-manage"></a>Définition des objets à gérer

Une fois que vous avez identifié la partie de votre entreprise à gérer, définissez les objets à gérer. La définition doit inclure les données requises et vous permettre d’implémenter les règles d’entreprise appropriées avec précision. Vous pouvez définir des objets à un niveau granulaire, mais il est préférable de choisir entre le niveau de détail contenu dans la définition et la nécessité de fournir suffisamment de détails pour être utiles. Les raccourcis au début du processus peuvent vous faire gagner du temps, mais peuvent être plus utilisés à l’avenir.

Le didacticiel CIM sur le site Web DMTF (Distributed Management Task Force) contient des informations d’excellence sur le processus de conception. Pour plus d’informations, consultez [www.dmtf.org](https://www.dmtf.org/).

Tenez compte des facteurs suivants lorsque vous développez et implémentez une conception de schéma :

-   Qualificateurs

    Les qualificateurs fournissent des informations sur la façon de décrire des classes, des objets, des propriétés, des méthodes et des paramètres. et elles sont appliquées aux définitions de classe et de propriété. Dans le code MOF, les qualificateurs sont placés entre crochets et peuvent inclure une \[ clé \] ou une \[ Association \] . Pour plus d’informations, consultez [Ajout d’un qualificateur](adding-a-qualifier.md) et [qualificateurs WMI](wmi-qualifiers.md).

-   Espace de noms

    Un espace de noms est une unité logique pour regrouper des classes et des objets, et pour contrôler la portée et la visibilité. En général, un espace de noms contient un ensemble de classes et d’objets qui représentent des objets managés dans un environnement spécifique. Pour plus d’informations, consultez [création de hiérarchies dans WMI](creating-hierarchies-within-wmi.md).

-   Object

    Un objet modélisé peut être un élément physique ou logique du schéma. Par exemple, vous pouvez modéliser un lecteur de disque physique, tel qu’un disque dur, ou un disque logique qui peut être une partition sur un disque physique. Une conception qui utilise une classe pour modéliser un lecteur de disque physique, puis étend cette classe pour modéliser un disque logique est plus extensible qu’une conception qui tente de créer une classe distincte pour chaque type de disque.

-   Données

    Les données peuvent être dynamiques ou statiques. Si les données sont dynamiques, vous devez créer un fournisseur de classes pour celle-ci.

    Pour permettre à l’utilisateur de modifier des données, vous devez déterminer si vous souhaitez ou non qu’une propriété soit directement accessible en écriture ou modifiable uniquement à l’aide d’une méthode appelée par l’utilisateur.

## <a name="defining-properties-or-methods"></a>Définition des propriétés ou des méthodes

En règle générale, une propriété de classe WMI est semblable à une propriété dans une classe C++. Si les seules actions que votre code implémente pour l’élément de données est d’obtenir la valeur ou de définir la valeur, les données doivent être définies en tant que propriété de la classe WMI.

Une méthode WMI effectue généralement une action qui modifie l’état d’un objet managé. Par exemple, si l’action consiste à activer ou désactiver l’opération d’un objet matériel, une méthode est probablement préférable à la création d’une propriété en lecture/écriture. Vous pouvez également décider de créer une propriété qui affiche l’état du matériel.

Lorsque vous créez une classe ou une instance, vous pouvez inclure des commentaires. Utilisez cette technique pour documenter votre classe ou expliquer vos techniques de programmation. Pour plus d’informations, consultez [création d’un commentaire](creating-a-comment.md). En outre, vous pouvez ajouter des données pour qualifier l’objectif d’un objet de données. Pour plus d’informations, consultez [Ajout d’un qualificateur](adding-a-qualifier.md).

## <a name="relating-objects-to-each-other"></a>Association d’objets entre eux

Il existe deux façons de lier des objets les uns aux autres : en créant des objets distincts et un objet Association qui les associe, ou en incorporant un objet dans l’autre. CIM ne prend pas en charge les objets incorporés. pour être conforme à la norme CIM, vous devez utiliser la première méthode. Toutefois, WMI prend en charge les objets incorporés. Utilisez l’une ou l’autre méthode pour représenter une relation entre les objets. Vous trouverez des exemples d’objets incorporés dans les [classes Win32](/windows/desktop/CIMWin32Prov/win32-provider). Par exemple, [**le \_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) a l’objet incorporé [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace), qui dispose d’un autre objet incorporé, [**Win32 \_ Trusted**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee).

Tenez compte des éléments suivants lorsque vous décidez de la façon de représenter des relations entre des objets :

-   Si une instance est utile par elle-même, une association fonctionne mieux. Par exemple, [**le \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) et [**Win32 \_ UserAccount**](/windows/desktop/CIMWin32Prov/win32-useraccount). Pour plus d’informations, consultez [déclaration d’une classe d’association](declaring-an-association-class.md).
-   Si une instance n’existe pas en dehors de l’objet parent, un objet incorporé fonctionne mieux. Par exemple, [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) et [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace). Pour plus d’informations, consultez [incorporation d’objets dans une classe](embedded-objects.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’un fournisseur WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Fourniture de données à WMI](providing-data-to-wmi.md)
</dt> <dt>

[Types de données MOF](mof-data-types.md)
</dt> </dl>

 

 
