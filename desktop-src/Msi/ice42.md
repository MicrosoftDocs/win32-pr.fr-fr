---
description: ICE42 valide que les serveurs InProc ne sont pas liés aux fichiers EXE dans la table de classe. Il vérifie également que seules les classes LocalServer et LocalServer32 ont des arguments et des valeurs DefInProc.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b913b92d82ad25a9722b289596f6b51940bbade55b5e544ebf636051e21b3ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581069"
---
# <a name="ice42"></a>ICE42

ICE42 valide que les serveurs InProc ne sont pas liés aux fichiers EXE dans la [table de classe](class-table.md). Il vérifie également que seules les classes LocalServer et LocalServer32 ont des arguments et des valeurs DefInProc.

## <a name="result"></a>Résultat

ICE42 publie une erreur si des serveurs InProc sont liés à des fichiers EXE dans la table de classe.

## <a name="example"></a>Exemples

ICE42 signale les erreurs suivantes pour l’exemple indiqué.



| Erreur ICE42                                                                                                                             | Description                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le CLSID « {GUID1} » est un serveur INPROC, mais le composant d’implémentation « Composant1 » a un EXE (« test.exe ») comme keyfile.                | Un fichier exécutable est spécifié en tant que serveur INPROC. Les fichiers EXE ne peuvent pas être des serveurs InProc.                                                                                                                            |
| Le CLSID « {GUID1} » dans le contexte « InProcServer32 » a un argument. Seuls les contextes LocalServer peuvent avoir des arguments.                              | Pour corriger cette erreur, supprimez l’argument.                                                                                                                                                                                   |
| Le CLSID « {GUID1} » dans le contexte « InProcServer32 » spécifie une valeur InProc par défaut. Seuls les contextes LocalServer peuvent avoir des valeurs InProc par défaut. | Il existe un objet avec une valeur InProc par défaut qui n’est pas un objet opérant dans les contextes LocalServer ou LocalServer32. Pour corriger cette erreur, supprimez la valeur DeflnProc ou modifiez le contexte de la classe.<br/> |



 

[Table de classe](class-table.md) (partielle)



| CLSID   | Contexte        | Composant\_ | DefInProcHandler | Argument |
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

 

 




