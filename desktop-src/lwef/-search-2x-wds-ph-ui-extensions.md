---
title: Ajout d’icônes et de menus contextuels avec des extensions de Shell
description: vous pouvez améliorer l’expérience de vos utilisateurs avec Microsoft Windows Desktop Search (WDS) et votre gestionnaire de protocole en implémentant des extensions de Shell.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9198fc56b8ca09e61909b1828d7d00b964bb12c0e13308583eb36a4e2211f3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976869"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a>Ajout d’icônes et de menus contextuels avec des extensions de Shell

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

vous pouvez améliorer l’expérience de vos utilisateurs avec Microsoft Windows Desktop Search (WDS) et votre gestionnaire de protocole en implémentant des extensions de Shell. Sans extension supplémentaire, le gestionnaire de protocole que vous créez n’inclut pas les expériences utilisateur suivantes :

-   WDS n’affiche pas d’icônes spécifiques pour vos résultats.
-   Lorsque les utilisateurs double-cliquent sur un élément, l’interface utilisateur ne répond pas à l’événement.
-   Quand les utilisateurs cliquent avec le bouton droit sur un élément, le menu contextuel ne prend en charge aucune opération pour l’élément.

Les implémentations minimales de **IPersist** et **IPersistFolder** sont requises par **IShellFolder**, et une implémentation minimale de **IShellFolder** est requise pour **IContextMenu** et **IExtractIcon**, les deux interfaces qui offrent une expérience utilisateur plus transparente.

 

## <a name="ipersist"></a>IPersist

L’interface **IPersist** définit la méthode unique **GetClassID**, conçue pour fournir le CLSID d’un objet qui peut être stocké de manière permanente dans le système.



| Méthode       | Description                                 |
|--------------|---------------------------------------------|
| GetClassID () | Retourne l’ClassID du gestionnaire de protocole |



 

> [!Note]
>
> Le même CLSID doit être implémenté pour **IPersist**, **IPersistFolder** et **IShellFolder**.

 

 

## <a name="ipersistfolder"></a>IPersistFolder

L’interface **IPersistFolder** est utilisée pour initialiser les objets de dossier de l’interpréteur de commandes. L’implémentation de cette interface, dérivée de **IPersist**, est la manière dont le dossier est indiqué à l’emplacement où il se trouve dans l’espace de noms Shell.



| Méthode       | Description                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| Initialize () | Demande à un objet de dossier de Shell de s’initialiser en fonction des informations transmises et des retours \_ OK |



 

> [!Note]
>
> Le même CLSID doit être implémenté pour **IPersist**, **IPersistFolder** et **IShellFolder**.

 

Vous n’utilisez pas cette interface directement. Elle est utilisée par l’implémentation du système de fichiers de l’interface IShellFolder :: BindToObject lors de l’initialisation d’un objet de dossier de l’interpréteur de commandes.

 

## <a name="ishellfolder"></a>IShellFolder

l’interface **IShellFolder** est utilisée pour gérer les dossiers, et une implémentation partielle est nécessaire pour que les interfaces d’icône et de contexte implémentées pour un gestionnaire de protocole se comportent correctement dans l’interface utilisateur des résultats de la recherche de bureau Windows. La plupart des fonctionnalités requises sont exposées par le biais de la méthode **GetUIObjectOf** . Cette méthode permet à un complément d’interroger les interfaces **IExtractIcon** et **IContextMenu** .

L’interface **IShellFolder** utilise PIDL à la place des URL. Contrairement aux spécifications d’une extension d’espace de noms complète, les compléments peuvent utiliser une structure IDL simple qui contient uniquement l’URL.

Les méthodes suivantes de **IShellFolder** doivent être implémentées. Notez que cinq de ces méthodes nécessitent une implémentation minimale.



| Méthode             | Description                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject()     | Retourne E \_ NOTIMPL                                                                                                                                                                                          |
| BindToStorage()    | Retourne E \_ NOTIMPL                                                                                                                                                                                          |
| CreateViewObject() | Retourne E \_ NOTIMPL                                                                                                                                                                                          |
| SetNameOf()        | Retourne E \_ NOTIMPL                                                                                                                                                                                          |
| ParseDisplayName() | Convertit une URL en structure PIDL                                                                                                                                                                        |
| CompareIDs()       | Compare deux valeurs PIDL                                                                                                                                                                                    |
| GetDisplayNameOf() | Retourne l’URL d’un PIDL                                                                                                                                                                                  |
| GetUIObjectOf()    | Cette méthode est similaire à la méthode QueryInterface OLE COM. Si une icône est demandée, l’appelant demande l’IID \_ IExtractIcon ; si un menu contextuel est demandé, l’appelant demande l' \_ IID IContextMenu. |



 

> [!Note]
>
> Le même CLSID doit être implémenté pour **IPersist**, **IPersistFolder** et **IShellFolder**.

 

**IShellFolder** n’est pas utilisé pour énumérer des dossiers. Cela signifie que le nom complet d’un dossier sera l’URL physique. Cela peut changer à l’avenir.

 

## <a name="icontextmenu"></a>IContextMenu

Lorsque WDS affiche les résultats à l’utilisateur, l’utilisateur peut cliquer avec le bouton droit sur un élément et afficher un menu contextuel défini par votre interface **IContextMenu** .

L’action par défaut dans le menu contextuel est la même que celle effectuée lors d’un double-clic sur l’élément. Sans les interfaces **IShellFolder** ou **IContextMenu** correspondantes pour l’élément, le comportement par défaut d’un événement de double-clic consiste à passer l’URL en tant qu’argument à la fonction ShellExecute.

 

## <a name="iextracticon"></a>IExtractIcon

**IExtractIcon** récupère une icône pour l’interface utilisateur WDS en fonction de l’URL figurant dans le PIDL fourni par votre gestionnaire de protocole.

 

## <a name="code-sample"></a>Exemple de code

L' [exemple de code d’interface utilisateur du gestionnaire de protocole personnalisé](-search-2x-wds-ph-ui-samplecode.md) illustre une implémentation de **IShellFolder** et des interfaces de prise en charge, et prend en charge la manipulation du PIDL.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Exemple de code d’interface utilisateur du gestionnaire de protocole personnalisé](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installation et inscription de gestionnaires de protocole](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




