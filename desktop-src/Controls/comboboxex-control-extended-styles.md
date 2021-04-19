---
title: Styles étendus de contrôle ComboBoxEx (CommCtrl. h)
description: Prendre en charge les styles étendus répertoriés dans cette section, ainsi que la plupart des styles de contrôle de zone de liste modifiable standard.
ms.assetid: 4741ac5e-1c46-4fd3-9174-b4ceb479261f
topic_type:
- apiref
api_name:
- CBES_EX_CASESENSITIVE
- CBES_EX_NOEDITIMAGE
- CBES_EX_NOEDITIMAGEINDENT
- CBES_EX_NOSIZELIMIT
- CBES_EX_PATHWORDBREAKPROC
- CBES_EX_TEXTENDELLIPSIS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71dc92264dbd1bd2f5a4b1136d9a6138e1fcffa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528115"
---
# <a name="comboboxex-control-extended-styles"></a>Styles étendus de contrôle ComboBoxEx

Prendre en charge les styles étendus répertoriés dans cette section, ainsi que la plupart des styles de contrôle de zone de liste modifiable standard.



| Constante                                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <dt>**CBES \_ ex \_ CaseSensitive**</dt> </dl>             | Les recherches **BSTR** dans la liste respectent la casse. Cela comprend les recherches à la suite du texte tapé dans la zone d’édition et du \_ message CB FindExactString.<br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <dt>**CBES \_ ex \_ NOEDITIMAGE**</dt> </dl>                   | La zone d’édition et la liste déroulante n’affichent pas d’images d’élément. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <dt>**CBES \_ ex \_ NOEDITIMAGEINDENT**</dt> </dl> | La zone d’édition et la liste déroulante n’affichent pas d’images d’élément. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <dt>**CBES \_ ex \_ NOSIZELIMIT**</dt> </dl>                   | Permet au contrôle ComboBoxEx d’être dimensionné verticalement plus petit que son contrôle de zone de liste déroulante contenu. Si la taille du ComboBoxEx est inférieure à celle de la zone de liste déroulante, la zone de liste déroulante est découpée. <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <dt>**CBES \_ ex \_ PATHWORDBREAKPROC**</dt> </dl> | Windows NT uniquement. La zone d’édition utilise la barre oblique (/), la barre oblique inverse ( \) et les caractères point (.) comme délimiteurs de mots. Ainsi, les raccourcis clavier pour le déplacement du curseur Word par mot sont effectifs dans les noms de chemin d’accès et les URL.<br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <dt>**CBES \_ ex \_ TEXTENDELLIPSIS**</dt> </dl>       | **Windows Vista et versions ultérieures.** Fait en sorte que les éléments dans la liste déroulante et la zone d’édition (lorsque la zone d’édition est en lecture seule) soient tronqués par des points de suspension (« ... ») et non simplement par le bord du contrôle. Cela est utile lorsque le contrôle doit être défini sur une largeur fixe, mais que les entrées de la liste peuvent être longues.<br/> |



## <a name="remarks"></a>Notes

Vous définissez et récupérez les styles étendus de ComboBox à l’aide des messages [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) et [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) .

> [!Note]  
> Si vous essayez de définir un style étendu pour un contrôle ComboBoxEx créé avec le style [**CBS \_ simple**](combo-box-styles.md) , il se peut qu’il ne redessine pas correctement. Le **style \_ simple CBS** ne fonctionne pas correctement avec le \_ \_ style étendu CBES ex PATHWORDBREAKPROC.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





