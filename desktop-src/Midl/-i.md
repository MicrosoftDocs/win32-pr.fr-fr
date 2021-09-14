---
title: Commutateur/i
description: Le commutateur/I spécifie les répertoires dans lesquels rechercher les fichiers IDL importés, les fichiers d’en-tête inclus et les fichiers ACF.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- MIDL du commutateur/i
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093926"
---
# <a name="i-switch"></a>Commutateur/i

Le commutateur **/i** spécifie les répertoires dans lesquels rechercher les fichiers IDL importés, les fichiers d’en-tête inclus et les fichiers ACF.

``` syntax
midl /I include_path
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*inclure le \_ chemin* 
</dt> <dd>

Spécifie un ou plusieurs répertoires qui contiennent des fichiers d’importation, d’inclusion et de CCP. L’espace blanc entre le commutateur **/i** et le *\_ chemin include* est facultatif. Séparez plusieurs répertoires par un point-virgule (;).

</dd> </dl>

## <a name="remarks"></a>Notes

Plusieurs répertoires peuvent apparaître avec chaque commutateur **/i** , et plusieurs commutateurs **/i** peuvent apparaître avec chaque appel du compilateur MIDL. Les répertoires sont recherchés dans l’ordre dans lequel ils sont spécifiés.

Le paramètre de commutateur **/i** est également passé par le compilateur MIDL au préprocesseur c du compilateur c. Lorsque le [**commutateur \_ /CPP cmd**](-cpp-cmd.md) est présent et que le commutateur [**/CPP \_ OPT**](-cpp-opt.md) n’est pas, le compilateur MIDL concatène la chaîne spécifiée par le commutateur **/CPP \_ cmd** avec les options **/i**, [**/d**](-d.md)et [**/u**](-u.md) et utilise cette chaîne concaténée pour appeler le préprocesseur C pour chaque fichier source IDL et ACF. Le commutateur du compilateur MIDL **/i** n’est pas passé au préprocesseur lorsque le commutateur du compilateur MIDL **/non \_ CPP** ou **/CPP \_ OPT** est spécifié.

dans les environnements de système d’exploitation Microsoft (64 bits Windows, 32 bits Windows, 16 bits Windows et MS-DOS), les répertoires sont recherchés dans l’ordre suivant :

1.  Répertoire actif
2.  Répertoires spécifiés par le commutateur **/i** (dans l’ordre suivant le commutateur)
3.  Répertoires spécifiés par la variable d’environnement INCLUDe

Lorsque les répertoires sont spécifiés avec le commutateur **/i** , le commutateur [**/non \_ Def \_ idir**](-no-def-idir.md) demande au compilateur MIDL d’ignorer le répertoire actif, d’ignorer les répertoires spécifiés par la variable d’environnement include et de rechercher uniquement les répertoires spécifiés.

Quand aucun répertoire n’est spécifié avec le commutateur **/i** , le commutateur [**/non \_ Def \_ idir**](-no-def-idir.md) demande au compilateur MIDL de rechercher uniquement le répertoire actif.

## <a name="examples"></a>Exemples

**MIDL/I c : \\ include ; c : \\ include \\ h/i \\ include2 nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/CPP \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/CPP \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/non \_ Def \_ idir**](-no-def-idir.md)
</dt> </dl>

 

 




