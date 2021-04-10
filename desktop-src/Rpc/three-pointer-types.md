---
title: Trois types pointeur
description: MIDL prend en charge trois types de pointeurs pour s’adapter à un large éventail d’applications.
ms.assetid: 6684c252-6fbe-49ca-9967-6d4baf5dc298
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efdcc9548568c8fca24d8abb40bf0eaa8b6e7da3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941034"
---
# <a name="three-pointer-types"></a>Trois types pointeur

MIDL prend en charge trois types de pointeurs pour s’adapter à un large éventail d’applications. Les trois niveaux différents sont appelés références, uniques et pointeurs complets, et sont indiqués par les attributs **\[** [**ref**](/windows/desktop/Midl/ref) **\]** , **\[** [**unique**](/windows/desktop/Midl/unique) **\]** et **\[** [**ptr**](/windows/desktop/Midl/ptr) **\]** , respectivement. Les classes de pointeur décrites par ces attributs s’excluent mutuellement. Les attributs de pointeur peuvent être appliqués aux pointeurs dans les définitions de type, les types de retour de fonction, les paramètres de fonction, les membres de structures ou d’unions, ou les éléments de tableau.

Les pointeurs incorporés sont des pointeurs qui sont membres de structures ou d’unions. Ils peuvent également être des éléments de tableaux. Dans le **\[** [](/windows/desktop/Midl/in) **\]** sens, les pointeurs **\[ Ref \]** incorporés sont supposés pointer vers un stockage valide et ne doivent pas avoir la valeur null. Cette situation s’applique de manière récursive à tous les pointeurs de **\[ référence \]** auxquels elles pointent. Dans le **\[ sens \]** , les pointeurs **\[ uniques \]** et complets incorporés (pointeurs avec l’attribut **\[ ptr \]** ) peuvent ou ne peuvent pas être null.

Tout attribut de pointeur placé sur un paramètre dans la syntaxe d’une déclaration de fonction affecte uniquement le déclarateur de pointeur le plus à droite pour ce paramètre. Pour affecter d’autres déclarateurs de pointeur, les types nommés intermédiaires doivent être utilisés.

Les fonctions qui retournent un pointeur peuvent avoir un attribut de pointeur comme attribut de fonction. Les attributs **\[ unique \]** et **\[ ptr \]** doivent être appliqués aux types de retour de fonction. Les déclarations de membres qui sont des pointeurs peuvent spécifier un attribut de pointeur comme attribut de champ. Un attribut de pointeur peut également être appliqué en tant qu’attribut de type dans les constructions [**typedef**](/windows/desktop/Midl/typedef) .

Quand aucun attribut de pointeur n’est spécifié en tant qu’attribut de champ ou de type, les attributs de pointeur sont appliqués selon les règles d’une déclaration de pointeur non attribute comme suit.

Dans le mode de compatibilité DCE, les attributs de pointeur sont déterminés dans le fichier IDL de définition. Si un **\[** attribut de [**pointeur \_ par défaut**](/windows/desktop/Midl/pointer-default)est **\]** spécifié dans l’interface de définition, cet attribut est utilisé. Si aucun attribut **\[ \_ par \] défaut de pointeur** n’est présent, tous les pointeurs non-attributs sont des pointeurs complets.

En mode extensions Microsoft, les attributs de pointeur peuvent être déterminés en important des fichiers IDL et sont appliqués dans l’ordre suivant :

1.  Attribut de pointeur explicite appliqué au site d’utilisation.
2.  Attribut **\[ Ref \]** , lorsque le pointeur sans attribut est un paramètre de pointeur de niveau supérieur.
3.  Attribut **\[ \_ par défaut \] de pointeur** spécifié dans l’interface de définition.
4.  Attribut **\[ \_ par défaut \] du pointeur** spécifié dans l’interface de base.
5.  Attribut **\[ unique \]** .

L' **\[** attribut d’interface [**\_ par défaut du pointeur**](/windows/desktop/Midl/pointer-default) **\]** spécifie les attributs de pointeur par défaut à appliquer à un déclarateur de pointeur dans un type, un paramètre ou une déclaration de type de retour lorsque cette déclaration n’a pas d’attribut de pointeur explicite appliqué. L’attribut d’interface **\[ \_ par défaut \] du pointeur** ne s’applique pas à un pointeur de niveau supérieur non attribut d’un paramètre, qui est supposé être **\[ Ref \]**.

 

 