---
description: Les applications COM+ comportent un ou plusieurs composants COM.
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: Parties d’une application COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483032"
---
# <a name="parts-of-a-com-application"></a>Parties d’une application COM+

Les applications COM+ comportent un ou plusieurs composants COM.

Les termes suivants sont utilisés dans la documentation COM+ :

<dl> <dt>

<span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*Composant COM*
</dt> <dd>

Unité binaire de code qui crée des objets COM (y compris le code d’empaquetage et d’inscription).

</dd> <dt>

<span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*Objet COM*
</dt> <dd>

Instance d’une classe COM.

</dd> <dt>

<span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*Classe COM*
</dt> <dd>

Implémentation concrète nommée d’une ou de plusieurs interfaces. Une classe COM est identifiée par un CLSID (parfois par un ProgID également).

</dd> <dt>

<span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*Interface COM*
</dt> <dd>

Groupe de fonctions de méthode associées exposées par une classe COM qui spécifient un contrat. Cela comprend le nom, la signature d’interface, la sémantique d’interface et le format de mémoire tampon de marshaling. Une interface est identifiée par un IID. La syntaxe de l’interface est définie dans les bibliothèques de types et/ou IDL. Les interfaces d’une classe COM doivent être divisées en ensembles de méthodes gérables et cohésifs.

Les interfaces COM sont immuables ; le contrat COM stipule qu’ils ne peuvent pas être modifiés. Toute modification (telle que l’ajout de méthodes) requiert la définition d’une nouvelle interface.

</dd> <dt>

<span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*Méthode COM*
</dt> <dd>

Un des ensembles de fonctions connexes fournies par une interface COM.

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a>Composants configurés et non configurés

Pour tirer parti des services pris en charge par les applications COM+, l’environnement COM+ impose des exigences spécifiques sur les composants COM créés pour les applications COM+. Lorsqu’il est ajouté à une application COM+, un composant COM est appelé *composant configuré*.

Les composants COM générés pour les applications COM+ sont des composants serveur in-process. Le composant doit contenir une bibliothèque de types (fichier. tlb) pour décrire toutes les classes implémentées dans le composant et déclarer les interfaces sur toutes les classes du composant. Vous pouvez créer et implémenter ces composants avec Microsoft Visual Basic, Microsoft Visual C++ ou n’importe quel outil de développement compatible COM.

Un *composant non configuré* est un composant qui n’est pas installé dans une application com+. Vous pouvez transformer les composants non configurés en composants configurés simplement en les intégrant dans une application COM+.

> [!Note]  
> N’utilisez pas la même AppID pour une application COM+ et dans le registre pour un composant non configuré. Lorsque le composant non configuré est activé, l’activation peut récupérer les informations de l’application COM+ à partir du Registre qui ne contient pas les informations requises pour l’activation COM. Des problèmes similaires peuvent survenir si un appel est passé à [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) à partir de Dllhost qui héberge une application serveur com+.

 

 

 
