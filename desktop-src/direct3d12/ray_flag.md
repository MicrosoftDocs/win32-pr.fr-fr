---
description: Indicateurs passés à la fonction TraceRay pour remplacer la transparence, l’élimination et le comportement précoce.
ms.assetid: ''
title: Énumération RAY_FLAG
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 31d6a002e5f3f4eeb5f86e671be0904d61cb916d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012910"
---
# <a name="ray_flag-enumeration"></a>\_Énumération d’indicateurs de rayon

Indicateurs passés à la fonction [**TraceRay**](traceray-function.md) pour remplacer la transparence, l’élimination et le comportement précoce.

## <a name="syntax"></a>Syntaxe


```
enum RAY_FLAG : uint
{
    RAY_FLAG_NONE                            = 0x00,
    RAY_FLAG_FORCE_OPAQUE                    = 0x01,
    RAY_FLAG_FORCE_NON_OPAQUE                = 0x02,
    RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH = 0x04,
    RAY_FLAG_SKIP_CLOSEST_HIT_SHADER         = 0x08,
    RAY_FLAG_CULL_BACK_FACING_TRIANGLES      = 0x10,
    RAY_FLAG_CULL_FRONT_FACING_TRIANGLES     = 0x20,
    RAY_FLAG_CULL_OPAQUE                     = 0x40,
    RAY_FLAG_CULL_NON_OPAQUE                 = 0x80,
}; 
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**indicateur de rayon \_ \_ aucun**
</dt> <dd>

Aucune option sélectionnée.

</dd> <dt>

<span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**indicateur de rayon \_ \_ force \_ opaque**
</dt> <dd>

Toutes les intersections de rayon-primitive rencontrées dans un raytrace sont traitées comme opaques.  Par conséquent, aucun nuanceur n’est exécuté, que la géométrie d’accès spécifie ou non l' \_ indicateur de géométrie D3D12 RAYTRACING \_ \_ \_ opaque, et quels que soient les indicateurs d’instance sur l’instance qui a été atteint.

Cet indicateur s’exclut mutuellement avec l’indicateur de rayon \_ \_ force \_ non opaque, l’élimination des indicateurs de \_ rayon \_ \_ \_ opaque et l’élimination des indicateurs de rayon \_ \_ \_ non \_ opaque.


</dd> <dt>

<span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**indicateur de rayon \_ \_ force \_ non \_ opaque**
</dt> <dd>

Toutes les intersections de rayon-primitive rencontrées dans un raytrace sont traitées comme non opaques.  Ainsi, tous les nuanceurs de correspondance, s’ils sont présents, sont exécutés indépendamment du fait que la géométrie d’accès spécifie l' \_ \_ indicateur de géométrie D3D12 RAYTRACING \_ \_ opaque et quels que soient les indicateurs d’instance sur l’instance qui a été atteint.
Cet indicateur s’exclut mutuellement avec l’indicateur de rayon \_ \_ FORCE_ \OPAQUE, les indicateurs de rayon, \_ \_ \_ les éliminations opaques et les indicateurs de rayon \_ \_ \_ non \_ opaques.


</dd> <dt>

<span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**\_indicateur \_ de rayon acceptant le \_ premier \_ accès et la \_ fin de la \_ \_ recherche**
</dt> <dd>

La première intersection de la primitive de Ray rencontrée dans un raytrace entraîne automatiquement l’appel de **AcceptHitAndEndSearch** juste après le nuanceur de correspondance, y compris s’il n’existe aucun nuanceur de correspondance. 
 
La seule exception est lorsque le nuanceur d’accès précédent appelle **IgnoreHit**. dans ce cas, le rayon continue non affecté, de telle sorte que l’accès suivant devient un autre candidat pour être le premier accès.  Pour que cette exception s’applique, le nuanceur de correspondance doit réellement être exécuté.  Par conséquent, si les nuanceurs de présence sont ignorés car l’accès est considéré comme opaque (par exemple, en raison de l’indicateur de rayon force opaque ou de l’indicateur de \_ \_ \_ \_ géométrie D3D12 RAYTRACING opaque \_ \_ \_ ou de l’indicateur d' \_ instance D3D12 RAYTRACING \_ \_ \_ opaque défini), **AcceptHitAndEndSearch** est appelé.

Si un nuanceur de correspondance le plus proche est présent lors du premier accès, il est appelé à moins que le nuanceur de l’indicateur de rayon \_ \_ \_ le plus proche \_ \_ soit également présent.  L’accès trouvé est considéré comme « le plus proche », même si d’autres résultats potentiels qui peuvent être plus proches sur le rayon n’ont peut-être pas été visités.

Une utilisation courante de cet indicateur concerne les ombres, où un seul accès doit être trouvé.


</dd> <dt>

<span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**indicateur de rayon \_ \_ Ignorer \_ le \_ nuanceur atteint le plus proche \_**
</dt> <dd>

Même si au moins un accès a été validé et si le groupe d’accès de l’accès le plus proche contient un nuanceur de correspondance le plus proche, ignorez l’exécution de ce nuanceur. 

</dd> <dt>

<span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**triangles de la réforme de l’indicateur de rayon \_ \_ \_ \_ \_**
</dt> <dd>

Active l’élimination des triangles retournés vers l’arrière. Consultez **\_ indicateurs d' \_ instance \_ D3D12 RAYTRACING** pour sélectionner les triangles de retour, par instance.

Sur les instances qui spécifient \_ \_ \_ la désactivation de l’indicateur d’instance D3D12 RAYTRACING \_ \_ \_ , cet indicateur n’a aucun effet.

Sur les types Geometry autres que D3D12 \_ RAYTRACING \_ Geometry \_ type \_ diangles, cet indicateur n’a aucun effet.

Cet indicateur s’exclut mutuellement avec \_ les \_ \_ \_ triangles frontaux de Culling de l’indicateur de rayon \_ .


</dd> <dt>

<span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**\_ \_ \_ triangles frontaux de Culling \_ \_ de l’indicateur de rayon**
</dt> <dd>

Active l’élimination des triangles frontaux. Consultez **\_ indicateurs d' \_ instance \_ D3D12 RAYTRACING** pour sélectionner les triangles de retour, par instance.

Sur les instances qui spécifient \_ \_ \_ la désactivation de l’indicateur d’instance D3D12 RAYTRACING \_ \_ \_ , cet indicateur n’a aucun effet.

Sur les types Geometry autres que D3D12 \_ RAYTRACING \_ Geometry \_ type \_ diangles, cet indicateur n’a aucun effet.

Cet indicateur s’exclut mutuellement avec \_ les \_ \_ \_ \_ triangles de retour de l’indicateur de rayon.


</dd> <dt>

<span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**indicateur de rayon d' \_ \_ élimination \_ opaque**
</dt> <dd>

Élimine toutes les primitives considérées comme opaques en fonction de leurs indicateurs Geometry et d’instance.

Cet indicateur s’exclut mutuellement avec l’indicateur de rayon \_ \_ force \_ opaque, l' \_ indicateur Ray \_ force \_ non \_ opaque et l’élimination des indicateurs de rayon \_ \_ \_ non \_ opaque.


</dd> <dt>

<span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**élimination d’indicateur de rayon \_ \_ \_ non \_ opaque**
</dt> <dd>

Élimine toutes les primitives considérées comme non opaques en fonction de leurs indicateurs Geometry et d’instance.

Cet indicateur s’exclut mutuellement avec l’indicateur de rayon \_ \_ force \_ opaque, l' \_ indicateur \_ de rayon force \_ non \_ opaque et l' \_ élimination opaque des indicateurs de rayon \_ \_ .


</dd>

## <a name="requirements"></a>Spécifications



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




