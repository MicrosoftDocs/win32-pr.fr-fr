---
description: ICE42 valide que les serveurs InProc ne sont pas liés aux fichiers EXE dans la table de classe. Il vérifie également que seules les classes LocalServer et LocalServer32 ont des arguments et des valeurs DefInProc.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539108"
---
# <a name="ice42"></a>ICE42

ICE42 valide que les serveurs InProc ne sont pas liés aux fichiers EXE dans la [table de classe](class-table.md). Il vérifie également que seules les classes LocalServer et LocalServer32 ont des arguments et des valeurs DefInProc.

## <a name="result"></a>Résultats

ICE42 publie une erreur si des serveurs InProc sont liés à des fichiers EXE dans la table de classe.

## <a name="example"></a>Exemple

ICE42 signale les erreurs suivantes pour l’exemple indiqué.



| Erreur ICE42                                                                                                                             | Description                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le CLSID « {GUID1} » est un serveur INPROC, mais le composant d’implémentation « Composant1 » a un EXE (« test.exe ») comme keyfile.                | Un fichier exécutable est spécifié en tant que serveur INPROC. Les fichiers EXE ne peuvent pas être des serveurs InProc.                                                                                                                            |
| Le CLSID « {GUID1} » dans le contexte « InProcServer32 » a un argument. Seuls les contextes LocalServer peuvent avoir des arguments.                              | Pour corriger cette erreur, supprimez l’argument.                                                                                                                                                                                   |
| Le CLSID « {GUID1} » dans le contexte « InProcServer32 » spécifie une valeur InProc par défaut. Seuls les contextes LocalServer peuvent avoir des valeurs InProc par défaut. | Il existe un objet avec une valeur InProc par défaut qui n’est pas un objet opérant dans les contextes LocalServer ou LocalServer32. Pour corriger cette erreur, supprimez la valeur DeflnProc ou modifiez le contexte de la classe.<br/> |



 

[Table de classe](class-table.md) (partielle)



| CLSID   | Context        | -\_ | DefInProcHandler | Argument |
|---------|----------------|-------------|------------------|----------|
| GUID1 | InProcServer32 | Composant1  | InProcServer     | Donnée      |



 

[Table des composants](component-table.md) (partielle)



| Composant  | KeyPath |
|------------|---------|
| Composant1 | Fichier1   |



 

[Table de fichiers](file-table.md) (partielle)



| Fichier  | Nom de fichier |
|-------|----------|
| Fichier1 | test.exe |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




