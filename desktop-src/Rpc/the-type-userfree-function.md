---
title: Fonction type_UserFree
description: La \_ fonction de type UserFree est une fonction d’assistance pour les attributs \ Wire \_ Marshal \ et \ user \_ Marshal \.
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727444"
---
# <a name="the-type_userfree-function"></a>Type \_ UserFree (fonction)

La fonction **<type> \_ UserFree** est une fonction d’assistance pour les attributs de marshaling de \[ [ \_ câble](/windows/desktop/Midl/wire-marshal) \] et d' \[ [utilisateur \_](/windows/desktop/Midl/user-marshal) \] . Les stubs appellent cette fonction pour libérer les données côté serveur. La fonction est définie comme suit :

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

Le <type> dans le nom de fonction correspond au type utilisateur spécifié dans la définition de type de marshaling de **\[ \_ \] câble** ou d' **\[ utilisateur \_ \]** .

Le paramètre *pFlags* est un pointeur vers un champ d’indicateur **long non signé** . Le mot supérieur de l’indicateur contient des indicateurs de représentation de données NDR tels que définis par l’ETCD OSF pour les représentations à virgule flottante, d’ordre d’octet et de caractère. Le mot inférieur contient un indicateur de contexte de marshaling tel que défini par le canal COM. La disposition exacte des indicateurs dans le champ est décrite dans [la fonction type d' \_ utilisateur](the-type-usersize-function.md).

Le paramètre *pMyObj* est un pointeur vers un objet de type utilisateur. Le moteur de NDR libère l’objet de niveau supérieur. Vous êtes responsable de la libération des objets sur lesquels l’objet de niveau supérieur peut pointer.

Les exceptions doivent être interceptées et gérées localement, les exceptions ne doivent pas être autorisées à propigated la pile des appels.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Marshal de câble \_](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[Marshal d’utilisateur \_](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 