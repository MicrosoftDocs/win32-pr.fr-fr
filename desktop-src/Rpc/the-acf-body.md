---
title: Corps ACF
description: Le corps ACF contient des attributs de configuration qui s’appliquent aux types et aux fonctions définis dans le corps de l’interface du fichier IDL.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1446b4f0e14849832766bc512a95d0ae0aeb249cebd814314b617ffa1e1125e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924619"
---
# <a name="the-acf-body"></a>Corps ACF

Le corps ACF contient des attributs de configuration qui s’appliquent aux types et aux fonctions définis dans le corps de l’interface du fichier IDL. Le corps du CCP peut être vide ou peut contenir des attributs d' [**inclusion**](/windows/desktop/Midl/include), de [**typedef**](/windows/desktop/Midl/typedef), de fonction et de paramètre ACF. Tous ces éléments sont facultatifs. Les attributs appliqués aux types et aux fonctions individuels dans le corps CCP remplacent les attributs dans l’en-tête ACF.

Le ACF spécifie le comportement sur l’ordinateur local et n’affecte pas les données transmises sur le réseau. Il est utilisé pour spécifier les détails d’un stub à générer. En mode de compatibilité DCE ([**/OSF**](/windows/desktop/Midl/-osf)), le ACF n’affecte pas l’interaction entre les stubs, mais entre le stub et le code d’application.

Un paramètre spécifié dans le CCP doit être l’un des paramètres spécifiés dans le fichier IDL. L’ordre de spécification du paramètre dans le ACF n’est pas significatif, car la correspondance est par nom, et non par position. La liste de paramètres dans le CCP peut être vide, même si la liste de paramètres de la signature IDL correspondante n’est pas (mais cela n’est pas recommandé). Les déclarateurs abstraits (paramètres sans nom) dans le fichier IDL font en sorte que le compilateur MIDL signale des erreurs lors du traitement du CCP, car le paramètre est introuvable.

La directive CCP **include** spécifie les fichiers d’en-tête à afficher dans l’en-tête généré dans le cadre d’une instruction **\# include** C-preprocesseur standard. Le mot clé ACF **include** est différent d’une directive **\# include** . Le mot clé ACF **include** entraîne l’affichage de la ligne «**\# include** *filename*» dans le fichier d’en-tête généré, tandis que la directive C «**\# include** *filename*» provoque le placement du contenu de ce fichier dans le CCP.

L’instruction CCP [**typedef**](/windows/desktop/Midl/typedef) vous permet d’appliquer des attributs de type ACF aux types précédemment définis dans le fichier IDL. La syntaxe de **typedef** ACF diffère de la syntaxe C **typedef** .

Les attributs de fonction ACF vous permettent de spécifier des attributs qui s’appliquent à la fonction dans son ensemble. Pour plus d’informations, consultez **\[** [**code**](/windows/desktop/Midl/code) **\]** , **\[** [**optimize**](/windows/desktop/Midl/optimize) **\]** et **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** .

Les attributs de paramètres ACF vous permettent de spécifier des attributs qui s’appliquent à des paramètres individuels de la fonction. Pour plus d’informations, consultez **\[** [**\_ nombre d’octets**](/windows/desktop/Midl/byte-count) **\]** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**configuration de/App \_**](/windows/desktop/Midl/-app-config)
</dt> <dt>

[**/osf**](/windows/desktop/Midl/-osf)
</dt> <dt>

[**\[\_handle automatique\]**](../midl/auto-handle.md)
</dt> <dt>

[**\[code\]**](../midl/code.md)
</dt> <dt>

[**\[\_handle explicite\]**](../midl/explicit-handle.md)
</dt> <dt>

[Fichier IDL (Interface Definition Language)](the-interface-definition-language-idl-file.md)
</dt> <dt>

[**\[handle implicite \_\]**](../midl/implicit-handle.md)
</dt> <dt>

[**inclusion**](/windows/desktop/Midl/include)
</dt> <dt>

[compilateur](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

[**\[SansCode\]**](../midl/nocode.md)
</dt> <dt>

[**\[requêtes\]**](../midl/optimize.md)
</dt> <dt>

[**\[représenter \_ comme\]**](../midl/represent-as.md)
</dt> <dt>

[**typedef**](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 