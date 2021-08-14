---
title: Structure des codes d’erreur COM
description: Structure des codes d’erreur COM
ms.assetid: 97e68708-eb62-4481-af03-cf8b80304103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65953582952ce076028ffcf6652e46356c4cf2afacdd088d546c2fdaafd18a33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104020"
---
# <a name="structure-of-com-error-codes"></a>Structure des codes d’erreur COM

L’illustration suivante montre le format d’un [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a) (ou SCODE); les nombres indiquent des positions de bits :

![Affiche le format d’un « résultat » ou d’un « CODE » avec des nombres indiquant les positions de bits.](images/a5a947d1-7b5a-4474-afed-2a1c58fe2421.png)

Le bit de poids fort dans **HRESULT** ou SCODE indique si la valeur de retour représente une réussite ou un échec. Si la valeur est 0, le niveau de gravité est \_ réussite, la valeur indique réussite. Si la valeur est 1, \_ erreur de gravité, elle indique un échec.

Les bits R, C, N et r sont réservés.

Le champ installation indique le service système responsable de l’erreur. Microsoft alloue de nouveaux codes d’installation à mesure qu’ils sont nécessaires. La plupart des valeurs SCODEs et **HRESULT** définissent le champ Facility sur Facility \_ ITF, indiquant une erreur de méthode d’interface.

Les champs d’installation courants sont décrits dans le tableau suivant.



| Champ d’installation                | Valeur        | Description                                                                                                                                                                                                                                                                                                              |
|-------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| répartition des installations \_<br/> | 2<br/> | Pour les erreurs d’interface **IDispatch** à liaison tardive. <br/>                                                                                                                                                                                                                                                             |
| ITF de l’installation \_<br/>      | 4<br/> | Pour la plupart des codes d’État retournés par les méthodes d’interface. La signification réelle de l’erreur est définie par l’interface. Autrement dit, deux valeurs **HRESULT** avec exactement la même valeur 32 bits retournée par deux interfaces différentes peuvent avoir des significations différentes. <br/>                                                       |
| NULL d’installation \_<br/>     | 0<br/> | Pour les codes d’État communs largement applicables tels que S \_ OK. <br/>                                                                                                                                                                                                                                                    |
| RPC de l’installation \_<br/>      | 1<br/> | Pour les codes d’État retournés par les appels de procédure distante. <br/>                                                                                                                                                                                                                                                       |
| stockage des installations \_<br/>  | 3<br/> | Pour les codes d’État renvoyés par les appels de méthode [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) relatifs au stockage structuré. Les codes d’État dont la valeur code (16 bits inférieurs) se trouvent dans la plage de codes d’erreur MS-DOS (autrement dit, inférieure à 256) ont la même signification que l’erreur MS-DOS correspondante. <br/> |
| INSTALLATION de \_ Win32<br/>    | 7<br/> | utilisé pour fournir un moyen de gérer les codes d’erreur des fonctions dans l’API Windows en tant que **HRESULT**. Les codes d’erreur dans OLE 16 bits qui dupliquaient les codes d’erreur système ont également été modifiés pour installer \_ Win32. <br/>                                                                                                 |
| fenêtres d’installation \_<br/>  | 8<br/> | Utilisé pour les codes d’erreur supplémentaires des interfaces définies par Microsoft.<br/>                                                                                                                                                                                                                                            |



 

Le champ de code est un numéro unique qui est assigné pour représenter l’erreur ou l’avertissement.

Par Convention, les valeurs **HRESULT** ont généralement des noms au format suivant : raison de la gravité de l' *installation* \_  \_ .

La *fonction* est soit le nom de la fonction, soit un autre identificateur distinctif ; La *gravité* est une seule lettre, S ou E, qui indique si l’appel de fonction a réussi ou a généré une erreur (E). et *reason* est un identificateur qui décrit la signification du code. Par exemple, le code d’État STG \_ E \_ FILENOTFOUND indique qu’une erreur liée au stockage s’est produite ; plus précisément, un fichier demandé n’existe pas. Codes d’état de \_ la fonction null omettre le préfixe de l' *installation* \_ .

Les codes d’erreur sont définis dans le contexte d’une implémentation d’interface. Une fois définis, les codes de réussite ne peuvent pas être modifiés ou de nouveaux codes de réussite ont été ajoutés. Toutefois, de nouveaux codes d’échec peuvent être écrits. Microsoft se réserve le droit de définir de nouveaux codes d’échec (mais pas des codes de réussite) pour les interfaces décrites dans \_ ITF ou dans les nouvelles installations.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des erreurs dans COM](error-handling-in-com.md)
</dt> <dt>

[Windows Protocoles : HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)
</dt> </dl>

 

