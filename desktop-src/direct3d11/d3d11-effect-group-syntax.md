---
title: Syntaxe des groupes d’effets (Direct3D 11)
description: Un groupe d’effets est déclaré avec la syntaxe décrite dans cette section.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c1b2c72b0a67a31911a0f2c9f9ae6ac0e9e20463a850c303dab4a208401d1c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069749"
---
# <a name="effect-group-syntax-direct3d-11"></a>Syntaxe des groupes d’effets (Direct3D 11)

Un groupe d’effets est déclaré avec la syntaxe décrite dans cette section.


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a>Paramètres



| Élément                                                                                                                                                                           | Description                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup<br/>                                                                                                         | mot clé equises.<br/>                                                                                                                                                                                                         |
| <span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName<br/>                                                                       | Obligatoire. Chaîne ASCII qui identifie de façon unique le nom du groupe d’effets. Contrairement aux techniques, les groupes doivent avoir des noms pour s’assurer que les techniques ont un identificateur unique (voir la section groupes et techniques ci-dessous).<br/> |
| <span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> Annotations de < ><br/> | \[\]facultatif. Un ou plusieurs éléments d’informations fournies par l’utilisateur (métadonnées) qui sont ignorés par le système d’effet. Pour obtenir la syntaxe, consultez syntaxe d’annotation (Direct3D 11). <br/>                                                      |
| <span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/>                                           | « Technique10 » ou « technique11 ». Les techniques qui utilisent les nouvelles fonctionnalités de Direct3D 11 (5 \_ nuanceurs, BindInterfaces, etc.) doivent utiliser « technique11 ».<br/>                                                                 |
| <span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName<br/>                                                       | Facultatif. Chaîne ASCII qui identifie de façon unique le nom de la technique d’effet. <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a>Groupes et techniques

Pour assurer la compatibilité avec les \_ effets FX 4 \_ 0, les groupes sont facultatifs. Il existe un groupe implicite nommé NULL entourant toutes les techniques globales.

Prenons l’exemple suivant :


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



En C++, il est possible d’obtenir une technique par nom de deux manières. Les commandes suivantes permettent de trouver les techniques évidentes :


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



Pour vous assurer que [**ID3DX11Effect :: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) fonctionne de la même façon que les effets 10, tous les groupes définis doivent avoir un nom.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](d3d11-effect-format.md)
</dt> <dt>

[Syntaxe d’effet technique (Direct3D 11)](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





