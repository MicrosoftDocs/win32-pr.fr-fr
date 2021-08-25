---
title: Options du compilateur MIDL
description: Options du compilateur MIDL
ms.assetid: a78505cf-cda6-4b41-abd1-2609aec4dcb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649cd96ffc0afa171ad218a737910ce15facbe0e9b5ef302dedb6615228bcf3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859329"
---
# <a name="midl-compiler-options"></a>Options du compilateur MIDL

Vous pouvez utiliser les options de ligne de commande suivantes pour substituer une partie du comportement par défaut du compilateur MIDL et choisir des optimisations appropriées pour votre application. Pour obtenir la liste complète des options de ligne de commande MIDL, consultez la [Référence du Command-Line MIDL](/windows/desktop/Midl/midl-command-line-reference).



| Commutateur de ligne de commande                                       | Description                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**/acf**](/windows/desktop/Midl/-acf)<br/>                          | Utilisez pour fournir un nom de fichier ACF explicite. Ce commutateur permet également l’utilisation de différents noms d’interface dans les fichiers IDL et ACF.<br/>                                                                                                       |
| [**/dlldata**](/windows/desktop/Midl/-dlldata)<br/>                  | Spécifie un nom de fichier pour le fichier de données DLL généré pour une DLL de proxy. Le nom de fichier par défaut est dlldata. c.<br/>                                                                                                                              |
| [**/env**](/windows/desktop/Midl/-env)<br/>                          | Dirige MIDL pour générer des stubs ou une bibliothèque de types pour un environnement cible.<br/>                                                                                                                                                            |
| [**/header**](/windows/desktop/Midl/-header), [ **/h**](/windows/desktop/Midl/-h)<br/> | Spécifie le nom du fichier d’en-tête d’interface. Le nom par défaut est celui du fichier IDL avec une extension. h.<br/>                                                                                                                       |
| [**/IID**](/windows/desktop/Midl/-iid)<br/>                          | Spécifie un nom de fichier d’identificateur d’interface qui remplace le nom de fichier d’identificateur d’interface par défaut pour une interface COM.<br/>                                                                                                              |
| [**/LCID**](/windows/desktop/Midl/-lcid)<br/>                        | Fournit une prise en charge complète des caractères DBCS afin que vous puissiez utiliser des caractères internationaux dans vos fichiers d’entrée, noms de fichiers et chemins d’accès aux répertoires.<br/>                                                                                                          |
| [**/non \_ format \_ opt**](/windows/desktop/Midl/-no-format-opt)<br/>    | Par défaut, pour réduire la taille du code, MIDL élimine les descripteurs en double. Ce commutateur désactive ce comportement d’optimisation.<br/>                                                                                                               |
| [**/OI**](/windows/desktop/Midl/-oi), **/OIC**, **/OIF**<br/>        | Indique à MIDL d’utiliser une méthode de marshaling entièrement interprétée. Les commutateurs/OIC et/Oicf fournissent des améliorations de performances supplémentaires.<br/>                                                                                                   |
| [**/out**](/windows/desktop/Midl/-out)<br/>                          | Spécifie le répertoire dans lequel le compilateur MIDL écrit les fichiers de sortie. Le répertoire de sortie peut être spécifié avec une lettre de lecteur, un chemin d’accès absolu ou les deux. La valeur par défaut est que MIDL écrit les fichiers dans le répertoire actif.<br/> |
| [**/proxy**](/windows/desktop/Midl/-proxy)<br/>                      | Spécifie le nom du fichier proxy d’une interface COM. Le nom par défaut est celui du fichier IDL plus « \_ p. c ».<br/>                                                                                                            |
| [**/TLB**](/windows/desktop/Midl/-tlb)<br/>                          | Spécifie le nom du fichier bibliothèque de types. Le nom par défaut est celui du fichier IDL, avec une extension. tlb.<br/>                                                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Compilation MIDL](midl-compilation.md)
</dt> </dl>

 

