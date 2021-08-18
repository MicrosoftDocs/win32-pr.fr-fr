---
title: Résolution des conflits de nom de fonction/propriété dans l’automatisation dans les extensions
description: Dans cette rubrique, \ 0034 ; objet \ 0034 ; indique l’objet, dans son ensemble, comme un client ADSI l’affiche. C’est-à-dire, ADSI et toutes ses extensions.
ms.assetid: 76207326-879e-408b-8004-06d940401a41
ms.tgt_platform: multiple
keywords:
- Résolution des conflits de noms de fonctions et de propriétés dans l’automatisation dans les extensions
- extensions ADSI, résolution des conflits de noms de fonctions et de propriétés dans Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53701c95672fe209cb57a15e3292e1269dc37e66e36f041110dd502f8a8a1486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637539"
---
# <a name="resolution-of-functionproperty-name-conflicts-in-automation-in-extensions"></a>Résolution des conflits de nom de fonction/propriété dans l’automatisation dans les extensions

Dans cette rubrique, « Object » indique l’objet, dans son ensemble, comme un client ADSI l’affiche. C’est-à-dire, ADSI et toutes ses extensions.

## <a name="same-function-name-with-the-same-parameters"></a>Même nom de fonction avec les mêmes paramètres

Si deux ou plusieurs interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) doubles dans un objet prennent en charge une propriété ou une méthode du même nom, par exemple, **func1**, l’appel est déterminé à l’aide des critères suivants. Si le client a un pointeur vers l’une des interfaces doubles qui prennent en charge une méthode appelée **func1** et si l’environnement d’automatisation prend en charge l’accès vtable, **func1** est appelé directement par le biais de l’accès vtable ADSI.

Si l’une des conditions ci-dessus a la valeur false, [**IDispatch :: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) et [**IDispatch :: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) sont appelés pour appeler **func1**.

Pour plus d’informations et pour obtenir une brève explication sur la façon dont un client peut ajouter un pointeur à une interface double, ainsi qu’une description des types d’environnements qui prennent en charge l’accès vtable, consultez [liaison tardive et accès à vtable dans le modèle d’extension ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).

Étant donné que tous les objets d’extension redirigent les fonctions [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) vers l’agrégateur, l’agrégateur contrôle l’appel de **func1** . Les règles sont les suivantes :

-   S’il n’existe aucune interface, et qu’il n’y aura qu’un seul, le cas échéant, dans l’agrégateur (ADSI) prend en charge une fonction appelée **func1**, l’agrégateur appelle son propre **func1**.
-   Dans le cas contraire, l’agrégateur parcourt chacune de ses extensions, dans l’ordre indiqué dans le registre, et recherche la première extension qui implémente une fonction appelée **func1**. Il est possible, mais improbable, que plusieurs interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) doubles dans cette première extension aient une fonction appelée **func1**. L’extension doit déterminer quel **func1** doit toujours être appelé dans Automation.

## <a name="same-function-name-with-different-parameters"></a>Même nom de fonction avec des paramètres différents

La section précédente a expliqué comment résoudre les conflits de nom de fonction, autrement dit, les noms de fonctions qui ont le même nom de fonction et la même liste de paramètres, tels que le nombre, le type et l’ordre, lorsqu’elle se produit dans Automation. Que se passe-t-il si deux fonctions ont le même nom mais des paramètres différents ? Si un client ADSI appelle la fonction à l’aide de [**IDispatch :: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) sans utiliser plusieurs noms pour spécifier les paramètres, le modèle d’extension ADSI ne peut pas lever l’ambiguïté des fonctions. En fonction du schéma de résolution abordé dans ci-dessus, la première extension du Registre qui prend en charge cette fonction par le biais de l’une de ses interfaces a sa version de cette fonction appelée, et l’appel peut échouer ou produire des résultats incorrects.

Par exemple :

-   Extn1 (premier dans le registre, sous la classe CA – priorité plus élevée) prend en charge **IInterface1**.
-   Extn2 (troisième dans le registre, sous la classe CA – priorité inférieure) prend en charge **IInterface2**.
-   **IInterface1** prend en charge **Method1 (int param1, int param2)**.
-   **IInterface2** prend en charge **Method1 (int param1)**.

Un client ADSI possède un pointeur d’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) vers un objet de classe ca. Il souhaite appeler **IInterface2 :: méthode1**. Si le client appelle « pDispatch->GetIDsOfNames (IID \_ null, rgszNames, 1, mon \_ LCID, rgDispId) » en stockant simplement le nom de fonction « méthode1 » dans *RgszNames \[ 0 \]*, **IInterface1 :: méthode1** au lieu de l' **IInterface2 souhaité :: méthode1** est appelé, et la fonction échoue car le nombre de paramètres est différent.

Pour réduire ce problème, les développeurs d’extensions peuvent préfixer leurs noms de fonction avec leurs propres identificateurs spécifiques et éviter les conceptions d’interface qui utilisent des fonctions du même nom, mais des paramètres différents.

En cas de conflit de noms, les clients ADSI peuvent éviter le problème par l’accès direct à la vtable si l’interface est une interface double. Si l’accès direct à vtable n’est pas possible, les clients ADSI doivent appeler [**IDispatch :: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) avec plusieurs noms, en spécifiant les noms de fonction ainsi que les paramètres du tableau *rgszNames* décrits précédemment.

Visual Basic 5 n’appelle pas la fonction [**IDispatch :: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) avec plusieurs noms. Autrement dit, il passe uniquement le nom de la fonction à **GetIDsOfNames**, mais pas aux arguments. toutefois, Visual Basic 5 permet aux utilisateurs d’appeler une fonction par l’accès direct à la vtable, au lieu d’appeler la fonction **IDispatch :: GetIDsOfNames** si l’interface est une interface double. Les développeurs doivent utiliser l’accès direct à la vtable, si possible.

Pour plus d’informations sur la résolution des conflits de noms, consultez l' [exemple relatif à la résolution des conflits de noms de fonctions](example-for-resolving-function-name-conflicts.md).

 

 