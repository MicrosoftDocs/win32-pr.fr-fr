---
title: Liaison tardive et accès vtable dans le modèle d’extension ADSI
description: Une interface double permet l’accès direct à toutes ses fonctions par le biais d’une interface de dispatch.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- liaison tardive et accès vtable dans le modèle d’extension ADSI ADSI
- ADSI d’extensions, liaison tardive ou accès vtable dans le modèle d’extension ADSI
- ADSI ADSI, exemple de code Visual Basic à l’aide de IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106513555"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a>Liaison tardive et accès vtable dans le modèle d’extension ADSI

Une interface double permet l’accès direct à toutes ses fonctions par le biais d’une interface de dispatch. Un client C/C++ peut interroger un pointeur d’interface double et utiliser l’accès direct à la vtable pour appeler ses fonctions. Cela permet un accès plus rapide que l’appel de la fonction à l’aide des fonctions [**IDispatch :: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) et [**IDispatch :: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) . Cela est particulièrement vrai dans le modèle d’extension, car toutes les interfaces doubles dans un objet d’extension doivent d’abord déléguer leurs fonctions **GetIDsOfNames** et **Invoke** à l’agrégateur (ADSI). L’agrégation doit alors effectuer des étapes internes supplémentaires pour identifier l’objet d’extension, éventuellement inclure l’agrégateur lui-même, la prise en charge de la fonction appelée et rediriger l’appel vers l’objet approprié.

Visual Basic appelle également une fonction à interface double à l’aide d’un accès direct à un vtable, s’il a un pointeur vers l’interface et un accès aux données de type à partir de la bibliothèque de types. Les clients ADSI écrits en Visual Basic peuvent spécifier un pointeur vers une interface double, par exemple [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explicitement, et ainsi activer l’accès vtable aux fonctions dans l’interface.


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



Comme une interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ne prend pas en charge l’accès vtable, cet exemple ne s’applique pas. Autrement dit, une fonction de répartition est toujours appelée par le biais des fonctions [**IDispatch :: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) et [**IDispatch :: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) uniquement.

Les versions actuelles de VBScript et JScript ne prennent pas non plus en charge l’accès vtable. Par conséquent, une interface double dans un environnement VBScript ou JScript fonctionne comme une interface de dispatch.

 

 