---
title: " dans, size_is et out, size_is prototype"
description: Le prototype de fonction suivant utilise deux chaînes comptées. Le développeur doit écrire du code sur le client et sur le serveur pour effectuer le suivi des longueurs de tableau de caractères et transmettre des paramètres qui indiquent aux stub le nombre d’éléments de tableau à transmettre.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03dbb4dd65d44122bea7ff086013295e0bf616d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229236"
---
# <a name="in-size_is-and-out-size_is-prototype"></a>\[dans, la taille \_ est \] et \[ sortante, la taille \_ est un \] prototype

Le prototype de fonction suivant utilise deux chaînes comptées. Le développeur doit écrire du code sur le client et sur le serveur pour effectuer le suivi des longueurs de tableau de caractères et transmettre des paramètres qui indiquent aux stub le nombre d’éléments de tableau à transmettre.

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

Notez que les paramètres qui décrivent la longueur du tableau sont transmis dans la même direction que les *tableaux : les* paramètres de la table de base de *achIn* sont des paramètres, \[ [](/windows/desktop/Midl/in) \] tandis que *pcbOut* et *achOut* sont des paramètres de \[ [**sortie**](/windows/desktop/Midl/out-idl) \] . En tant que paramètre de **\[ \] sortie** , le paramètre *PcbOut* doit suivre la Convention C et être déclaré comme pointeur.

Le code client compte le nombre de caractères de la chaîne, y compris le zéro de fin, avant d’appeler la procédure distante comme indiqué ci-dessous :

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

La procédure distante sur le serveur fournit la longueur de la mémoire tampon de retour dans *cbOut* , comme indiqué ci-dessous :

``` syntax
/* server */
void Analyze(char *pchIn,
             long cbIn,
             char *pchOut,
             long *pcbOut)
{
   ...
   *pcbOut = strlen(pchOut) + 1; // transmitted elements
   return;
}
```

L' \[ attribut de **chaîne** \] peut être utilisé lorsqu’un paramètre est considéré comme une chaîne. Cet attribut indique au stub de calculer la taille de la chaîne, ce qui élimine la surcharge associée à la \[ [**longueur**](/windows/desktop/Midl/size-is) des \] paramètres. En outre, il dirige le stub pour vérifier que la chaîne se termine par **null** avant de passer le paramètre à l’application.

 

 