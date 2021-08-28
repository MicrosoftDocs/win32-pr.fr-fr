---
title: Commutateur/backward_compat
description: Le \_ commutateur de compatibilité/Backward indique au compilateur MIDL de désactiver certaines fonctionnalités avancées lors de la génération de stubs RPC/com.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd412bdabe4255a9a4538503b29ddf5681265ce5e16c81d3d5fc2484eb6c9675
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086389"
---
# <a name="backward_compat-switch"></a>\_commutateur de compatibilité/Backward

Le \_ commutateur de compatibilité/Backward indique au compilateur MIDL de désactiver certaines fonctionnalités avancées lors de la génération de stubs RPC/com.

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a>Options de commutateur

*taille de MAYBENULL \_*<dl> Applique l’attribut de [ \[ désactivation de la \_ \_ \] vérification de cohérence](disable-consistence-check.md) à une compilation MIDL entière.  
</dl>

*zeroout \_ alignmentgap*<dl> Désactive les écarts de zéro dans la mémoire tampon marshalée.  
</dl>

*Séquence \_ d' \_ échappement ByValue BSTR*<dl> Indique au compilateur MIDL d’honorer les séquences d’échappement, telles que â € ̃ \\ nâ,™ ou â € ̃ \\ t €™ in BSTR.  
</dl>

*DefaultValue de chaîne \_*<dl> Force le compilateur MIDL à contraindre les chaînes des attributs [**\[ DEFAULTVALUE \]**](defaultvalue.md) en variant. \_Type VT I4 avant de convertir la valeur en type correct.  
</dl>

*\_WCHAR \_ t signé*<dl> Dirige MIDL pour traiter le type WCHAR \_ t comme signé pour la compatibilité avec Visual Basic.  
</dl>

## <a name="remarks"></a>Remarques

-   *\_ taille de MAYBENULL*: voir \[ désactiver \_ la \_ vérification de cohérence \] .
-   *zeroout \_ alignmentgap*: lorsque IDLs sont compilés avec â € «Target nt60 ou version ultérieure, MIDL crée des stubs qui éliminent les éventuels écarts d’alignement entre les membres ou une structure dans la mémoire tampon de câble. Le commutateur de ligne de commande */Backward \_ compat zeroout \_ alignmentgap* dirige MIDL pour désactiver cette fonctionnalité.

    Dans l’exemple de structure suivant, la mémoire tampon de câble contient un intervalle d’alignement de 7 octets pour aligner le membre hyper sur 8 après le membre char. Avec â € «Target NT60 ou version ultérieure, MIDL aura zéro ce fossé, sauf si le commutateur est utilisé.

    Fichier IDL :

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    Ce commutateur peut apporter une légère amélioration des performances avec des augmentations potentiellement significatives du risque de divulgation.

-   Type d' *\_ \_ échappement BSTR ByValue*: par défaut, le compilateur MIDL ne traite pas les séquences d’échappement telles que â € ̃ \\ nâ,™ ou â € ̃ \\ ™ t dans les constantes de chaîne pour OLE Automation lors de la conversion d’une constante de chaîne en types VT \_ LPSTR ou VT \_ LPWStr. Avec cette option de commutateur de compatibilité descendante, les séquences d’échappement sont évaluées.
-   *String \_ DefaultValue*: force le compilateur MIDL à contraindre les chaînes numériques des attributs [**\[ \] DefaultValue**](defaultvalue.md) en variant. \_Type VT I4 avant de convertir la valeur en type correct. Cela peut entraîner une perte de précision dans certains cas. par conséquent, cette option de commutation n’est pas recommandée.
-   *\_ WCHAR \_ t signé*: demande à MIDL de traiter le \_ type WCHAR t comme signé pour la compatibilité avec Visual Basic.

 

 




