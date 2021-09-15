---
description: Utilisation des extensions de Shell pour implémenter un gestionnaire de raccordement de copie.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Comment créer des gestionnaires de raccordement de copie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530420"
---
# <a name="how-to-create-copy-hook-handlers"></a>Comment créer des gestionnaires de raccordement de copie

Les procédures générales d’implémentation et d’inscription d’un gestionnaire d’extensions de Shell sont décrites dans [création de gestionnaires d’extensions de Shell](handlers.md). Ce document se concentre sur les aspects de l’implémentation qui sont spécifiques aux gestionnaires de raccordement de copie.

-   [Implémentation des gestionnaires de raccordement de copie](#step-1-implementing-copy-hook-handlers)
-   [Inscription des gestionnaires de raccordement de copie](#step-2-registering-copy-hook-handlers)
-   [Rubriques connexes](#related-topics)

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-copy-hook-handlers"></a>Étape 1 : implémentation des gestionnaires de raccordement de copie

Comme tous les gestionnaires d’extensions de Shell, les gestionnaires de raccordement de copie sont des objets COM (Component Object Model) in-process implémentés en tant que dll. Ils exportent une interface en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)). L’interpréteur de commandes Initialise le gestionnaire directement, donc il n’est pas nécessaire d’utiliser une interface d’initialisation telle que [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).

L’interface [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) a une seule méthode, [**ICopyHook :: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)). Quand un dossier va être déplacé, l’interpréteur de commandes appelle cette méthode. Elle transmet diverses informations, notamment :

-   Nom du dossier.
-   Nom de la destination ou du nouveau dossier.
-   Opération tentée.
-   Attributs des dossiers source et de destination.
-   Handle de fenêtre qui peut être utilisé pour afficher une interface utilisateur.

Quand la méthode [**ICopyHook :: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) de votre gestionnaire est appelée, elle retourne l’une des trois valeurs suivantes pour indiquer à l’interpréteur comment il doit continuer.



| Valeur    | Description                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| IDYES    | Autorise l’opération.                                                                                                                            |
| IDNO     | Empêche l’opération sur ce dossier. L’interpréteur de commandes peut continuer avec toutes les autres opérations qui ont été approuvées, telles qu’une opération de copie par lot. |
| IDCANCEL | Empêche l’opération en cours et annule toutes les opérations en attente.                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a>Étape 2 : inscription des gestionnaires de raccordement de copie

Les gestionnaires de raccordement de copie pour les dossiers sont enregistrés sous la **\_ \_** \\  \\  \\ sous-clé de shellex **CopyHookHandlers** du répertoire racine de la classe HKEY. Créez une sous-clé de **CopyHookHandlers** nommée pour le gestionnaire et définissez la valeur par défaut de la sous-clé sur la forme de chaîne du GUID de l’identificateur de classe (CLSID) du gestionnaire.

L’exemple suivant ajoute la sous-clé **MyCopyHandler** à la liste des gestionnaires de raccordement de copie de l’interpréteur de commandes.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

Les gestionnaires de raccordement de copie pour les objets d’imprimante sont enregistrés de la même façon. La seule différence réside dans le fait que vous devez les inscrire sous la sous-clé des imprimantes **\_ \_ racines de la classe HKEY** \\  .

## <a name="remarks"></a>Notes

Normalement, les utilisateurs et les applications peuvent copier, déplacer, supprimer ou renommer des dossiers avec peu de restrictions. En implémentant un gestionnaire de raccordement de copie, vous pouvez contrôler si ces opérations ont lieu. Par exemple, l’implémentation de ce type de gestionnaire vous permet d’empêcher le renommage ou la suppression de dossiers critiques. Les gestionnaires de raccordement de copie peuvent également être implémentés pour les objets d’imprimante.

Les gestionnaires de raccordement de copie sont globaux. L’interpréteur de commandes appelle tous les gestionnaires enregistrés chaque fois qu’une application ou un utilisateur tente de copier, déplacer, supprimer ou renommer un dossier ou un objet imprimante. Le gestionnaire n’effectue pas l’opération elle-même. Elle l’approuve ou la refuse. Si tous les gestionnaires approuvent, l’interpréteur de commandes effectue l’opération. Si un gestionnaire refuse l’opération, il est annulé et les gestionnaires restants ne sont pas appelés. Les gestionnaires de raccordement de copie ne sont pas informés de la réussite ou de l’échec de l’opération. ils ne peuvent donc pas être utilisés pour surveiller les opérations de fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de gestionnaires d’extensions d’environnement](handlers.md)
</dt> <dt>

[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))
</dt> </dl>

 

 
