---
title: Fonction type_UserSize
description: La \_ fonction type d’utilisateur est une fonction d’assistance pour les attributs \ Wire \_ Marshal \ et \ user \_ Marshal \.
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f997d12e11f643eb2faf9990454a8508d15636
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886050"
---
# <a name="the-type_usersize-function"></a>La fonction type d' \_ utilisateur

La fonction **&lt; type &gt; \_** d’utilisateur est une fonction d’assistance pour les attributs de marshaling de \[ [ \_ câble](/windows/desktop/Midl/wire-marshal) \] et d' \[ [utilisateur \_](/windows/desktop/Midl/user-marshal) \] . Les stubs appellent cette fonction pour dimensionner la mémoire tampon de données RPC pour l’objet de données utilisateur avant que les données ne soient marshalées côté client ou côté serveur. La fonction est définie comme suit :

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

Le &lt; type &gt; dans le nom de fonction correspond à user-type, comme spécifié dans la définition de type de marshaling de **\[ câble \_ \]** ou d' **\[ utilisateur \_ \]** . Ce type peut être non transmissible ou même, lorsqu’il est utilisé avec l’attribut de **\[ \_ Marshal \] utilisateur** , inconnu du compilateur MIDL. Le nom du type de câble (le nom du type transmis sur le réseau) n’est pas utilisé dans le prototype de la fonction. Notez, toutefois, que le type de câble définit la disposition des données comme spécifié par l’ETCD OSF. Toutes les données doivent être converties au format de représentation de données réseau (NDR).

Le paramètre *pFlags* est un pointeur vers un champ d’indicateur **long non signé** . Le mot supérieur de l’indicateur contient des indicateurs de format NDR tels que définis par l’ETCD OSF pour les représentations à virgule flottante, d’ordre d’octet et de caractère. Le mot inférieur contient un indicateur de contexte de marshaling tel que défini par le canal COM. La disposition exacte des indicateurs dans le champ est indiquée dans le tableau suivant.



| Bits  | Indicateur                                  | Valeur                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| 31-24 | Représentation à virgule flottante         | 0 = IEEE 1 = VAX 2 = Cray 3 = IBM                                                         |
| 23-20 | Ordre des octets à virgule flottante et entier | 0 = Big-endian 1 = Little endian                                                          |
| 19-16 | Représentation de caractères              | 0 = ASCII 1 = EBCDIC                                                                      |
| 15-0  | Indicateur de contexte de marshaling               | 0 = MSHCTX \_ local 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ InProc |



 

L’indicateur de contexte de marshaling permet de modifier le comportement de votre routine en fonction du contexte de l’appel RPC. Par exemple, si vous avez un handle (**long**) vers un bloc de données, vous pouvez envoyer le descripteur pour un appel in-process, mais vous enverrez les données réelles pour un appel à un autre ordinateur. L’indicateur de contexte de marshaling et ses valeurs sont définis dans les fichiers Wtypes. h et Wtypes. idl dans le kit de développement logiciel (SDK) de la plateforme.

> [!Note]  
> Lorsque le type de câble est correctement défini, il n’est pas nécessaire d’utiliser les indicateurs de format NDR, car le moteur de NDR effectue les conversions nécessaires.

 

Le *StartingSize* un paramètre est l’offset de la mémoire tampon actuelle. La taille de départ indique l’offset de la mémoire tampon pour l’objet utilisateur, et elle peut ou non être correctement alignée. Votre routine doit tenir compte de ce qui est nécessaire.

Le paramètre *pMyObj* est un pointeur vers un objet de type utilisateur.

La valeur de retour est la nouvelle position de décalage ou de mémoire tampon. La fonction doit retourner la taille cumulée, qui correspond à la taille de départ et au remplissage possible plus la taille des données.

La fonction **&lt; type &gt; \_ Users** peut retourner un surestime de la taille nécessaire. La taille réelle de la mémoire tampon envoyée est définie par la taille des données, et non par la taille d’allocation de la mémoire tampon.

La fonction **&lt; type d' &gt; \_ utilisateur** n’est pas appelée si la taille du câble peut être calculée au moment de la compilation. Notez que pour la plupart des unions, même s’il n’y a pas de pointeurs, la taille réelle de la représentation de câble ne peut être déterminée qu’au moment de l’exécution.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Marshal d’utilisateur \_](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[Marshal de câble \_](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 
