---
title: commutateur/cpp_cmd
description: Le \_ commutateur/CPP cmd spécifie le préprocesseur que le compilateur MIDL utilise pour prétraiter les fichiers d’entrée.
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /commutateur cpp_cmd MIDL
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678665"
---
# <a name="cpp_cmd-switch"></a>\_commutateur cmd/CPP

Le commutateur **/CPP \_ cmd** spécifie le préprocesseur que le compilateur MIDL utilise pour prétraiter les fichiers d’entrée.

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*\_Binaire de préprocesseur \_ C* 
</dt> <dd>

Spécifie la commande qui appelle le préprocesseur. Cette commande permet aux développeurs de remplacer le préprocesseur par défaut. Par défaut, MIDL appelle le compilateur Microsoft C/C++ à partir de l’environnement de génération de l’ordinateur de Build.

</dd> </dl>

## <a name="remarks"></a>Notes

L' *argument \_ \_ binaire du préprocesseur C* du commutateur peut spécifier le chemin d’accès complet ; le suffixe et les guillemets de l’exe sont facultatifs. En règle générale, les développeurs utilisent le commutateur pour choisir une version particulière du préprocesseur Microsoft C/C++ ou équivalent dans l’environnement de génération. Dans ce cas, il n’est pas nécessaire d’utiliser le commutateur [**/CPP \_ OPT**](-cpp-opt.md) avec **/CPP \_ cmd**.

Lors de l’utilisation d’un préprocesseur non-Microsoft, en particulier lorsque le préprocesseur spécifié ne dirige pas sa sortie vers stdout, le commutateur du compilateur C qui redirige la sortie vers stdout dans le cadre du commutateur [**/CPP \_ OPT**](-cpp-opt.md) du compilateur MIDL doit être spécifié. Pour plus d’informations [, consultez Configuration requise pour le préprocesseur C pour MIDL](c-preprocessor-requirements-for-midl.md)

Le préprocesseur est appelé par une chaîne de commande qui est formée à partir des informations fournies au compilateur MIDL par **/CPP \_ cmd**, [**/CPP \_ OPT**](-cpp-opt.md), [**/d**](-d.md), [**/i**](-i.md)et [**/u**](-u.md) commutateurs. Le tableau suivant résume la construction de la chaîne de commande pour chaque combinaison de commutateurs **/CPP \_ cmd** et **/CPP \_ OPT** .

Lorsque le commutateur **/CPP \_ cmd** n’est pas spécifié, le compilateur MIDL appelle le compilateur Microsoft C/C++. MIDL utilise un binaire Cl.exe trouvé dans l’environnement de génération.

Quand le commutateur [**/CPP \_ OPT**](-cpp-opt.md) n’est pas présent, le compilateur MIDL concatène la chaîne spécifiée par le **commutateur \_ /CPP cmd** avec les informations spécifiées par les options MIDL [**/i**](-i.md), [**/d**](-d.md) et [**/u**](-u.md) . La chaîne/E est également concaténée à la chaîne d’appel du compilateur C pour indiquer que le compilateur C/C++ doit effectuer un prétraitement uniquement. Le commutateur [**/nologo**](-nologo.md) est ajouté pour supprimer la bannière du compilateur C/C++. Le compilateur MIDL utilise la chaîne concaténée pour appeler le préprocesseur C pour le fichier IDL de niveau supérieur, ainsi que pour les fichiers IDL importés, ainsi que pour tous les fichiers ACF existants.

Quand le commutateur [**/CPP \_ OPT**](-cpp-opt.md) est présent, ce qui doit être un cas rare pour les plateformes actuelles 32 bits et 64 bits, le compilateur MIDL concatène la chaîne spécifiée par le commutateur **/CPP \_ cmd** avec la chaîne spécifiée par le commutateur d’activation **/CPP \_** . Le compilateur MIDL utilise la chaîne concaténée pour appeler le binaire de préprocesseur indiqué à la place du préprocesseur par défaut. Lorsque le **commutateur/CPP \_ OPT** est présent, ni les options du compilateur MIDL spécifiées par les commutateurs [**/I**](-i.md), [**/d**](-d.md)et [**/U**](-u.md) , ni le commutateur/e du compilateur C ne sont concaténées avec la chaîne. Vous devez fournir l’option/E, ou équivalent, dans le cadre de la chaîne.



| /CPP \_ cmd est présent ? | /CPP \_ OPT est présent ? | Description                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Non (par défaut)       | Non (par défaut)       | Appelle le compilateur Microsoft C/C++ par défaut avec les paramètres obtenus à partir des commutateurs MIDL [**/i**](-i.md), [**/d**](-d.md) et [**/u**](-u.md) . Ajoute les commutateurs de préprocesseur/E et [**/nologo**](-nologo.md). |
| Oui                | Non                 | Appelle le binaire de préprocesseur indiqué avec les mêmes commutateurs que ci-dessus.                                                                                                                                        |
| Non                 | Oui                | Appelle le compilateur Microsoft C avec les options spécifiées. N’utilise pas les options MIDL [**/i**](-i.md), [**/d**](-d.md), [**/u**](-u.md) . Vous devez fournir/E dans le cadre de l’option [**/CPP \_ OPT**](-cpp-opt.md).             |
| Oui                | Oui                | Appelle le binaire de préprocesseur spécifié avec les options spécifiées uniquement. Vous devez utiliser des guillemets.                                                                                                                       |



 

## <a name="examples"></a>Exemples

**MIDL/CPP \_ cmd d : \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC : \\ Inc filename. idl**

**MIDL/CPP \_ cmd "mycpp"/DFLAG = true/IC : \\ Inc filename. idl**

**MIDL/CPP \_ OPT "/E/DFLAG = true/IC : \\ Inc" nom_fichier. idl**

**MIDL/CPP \_ cmd "cl"/CPP \_ OPT "/e/DFLAG = true/IC : \\ Inc" nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/CPP \_ opt**](-cpp-opt.md)
</dt> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/non \_ CPP**](-no-cpp-nocpp.md)
</dt> <dt>

[C-Configuration requise pour le préprocesseur pour MIDL](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




