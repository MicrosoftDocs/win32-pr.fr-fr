---
description: Il existe un certain nombre de requêtes intéressantes sur un pilote qu’une application peut prendre en cas de baisse des performances.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Notification asynchrone (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998741"
---
# <a name="asynchronous-notification-direct3d-9"></a>Notification asynchrone (Direct3D 9)

Il existe un certain nombre de requêtes intéressantes sur un pilote qu’une application peut prendre en cas de baisse des performances. Dans Direct3D 7 et Direct3D 8, un mécanisme de requête synchrone, GetInfo, fonctionnait bien pour des statistiques, mais aucune requête critique pour les performances n’a été ajoutée. Il existe d’autres éléments (tels que des délimiteurs) qui sont intrinsèquement asynchrones. Il s’agit d’une API simple pour effectuer des requêtes synchrones et asynchrones. GetInfo sera mis hors service dans Direct3D 9.

Créez une requête à l’aide de [**IDirect3DDevice9 :: CreateQuery**](/windows/desktop/api). Cette méthode prend un D3DQUERYTYPE, qui définit le type de requête à créer et retourne un pointeur vers un objet [**IDirect3DQuery9**](/windows/desktop/api) . Si le type de requête n’est pas pris en charge, l’appel retourne une erreur D3DERR \_ NOTAVAILABLE. À l’aide de l’objet de requête, l’application soumet la requête au runtime à l’aide de [**IDirect3DQuery9 :: issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue), et interroge l’état de la requête à l’aide de [**IDirect3DQuery9 :: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Si le résultat de la requête est disponible, S \_ OK est retourné ; sinon, s \_ false est retourné. L’application est censée passer une mémoire tampon de taille appropriée pour les résultats de la requête.

L’application a la possibilité de forcer le runtime à vider la requête au pilote à l’aide de D3DGETDATA \_ flush avec [**IDirect3DQuery9 :: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Elle provoque un vidage, forçant le pilote à voir la requête. Dans ce cas, D3DERR \_ DEVICELOST est retourné si l’appareil est perdu.

Toutes les requêtes sont perdues lorsque l’appareil est perdu, l’application doit les recréer. Si l’appareil ne prend pas en charge la requête et que pQueryID a la **valeur null**, la création de la requête échoue avec D3DERR \_ INVALIDCALL.

Le tableau suivant récapitule les informations importantes sur chaque type de requête.



| QuertyType                    | Indicateur de problème valide              | Mémoire tampon GetData              | Runtime      | Début de requête implicite |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| D3DQUERYTYPE \_ Vcache          | Fin de D3DISSUE \_                 | D3DDEVINFO \_ Vcache          | Vente au détail/débogage | CreateDevice                |
| D3DQUERYTYPE \_ ResourceManager | Fin de D3DISSUE \_                 | D3DDEVINFO \_ ResourceManager | Déboguer uniquement   | Présent                     |
| D3DQUERYTYPE \_ VERTEXSTATS     | Fin de D3DISSUE \_                 | D3DDEVINFO \_ D3DVERTEXSTATS  | Déboguer uniquement   | Présent                     |
| \_Événement D3DQUERYTYPE           | Fin de D3DISSUE \_                 | BOOL                        | Vente au détail/débogage | CreateDevice                |
| \_Occlusion D3DQUERYTYPE       | D3DISSUE \_ Begin, D3DISSUE \_ end | DWORD                       | Vente au détail/débogage | N/A                         |



 

Champ Flags pour [**IDirect3DQuery9 :: issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



Champ Flags pour [**IDirect3DQuery9 :: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Astuces de programmation](programming-tips.md)
</dt> </dl>

 

 
