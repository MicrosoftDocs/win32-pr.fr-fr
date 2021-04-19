---
title: Syntaxe
description: Voici la syntaxe d’appel de FXC.exe, l’outil Effect-compiler. Pour obtenir un exemple, consultez Compilation hors connexion.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- fxc, syntaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "106511104"
---
# <a name="syntax"></a>Syntaxe

Voici la syntaxe d’appel de FXC.exe, l’outil Effect-compiler. Pour obtenir un exemple, consultez [compilation hors connexion](dx-graphics-tools-fxc-using.md).

-   [Utilisation](#usage)
-   [Arguments](#arguments)
-   [Remarques](#remarks)
-   [Profils](#profiles)
-   [Notes de version](#version-notes)
-   [Rubriques connexes](#related-topics)

## <a name="usage"></a>Utilisation

**fxc** *SwitchOptions* *nom de fichier*

## <a name="arguments"></a>Arguments
Séparez chaque option de commutateur par un espace ou un signe deux-points.

### <a name="switchoptions"></a>*SwitchOptions*
\[dans les \] options de compilation. Il n’existe qu’une seule option obligatoire, et bien d’autres sont facultatives. Séparez-les par un espace ou un signe deux-points.

#### <a name="required-option"></a>Option obligatoire
##### <a name="t-profile"></a>/T <*Profil*>
Modèle de nuanceur (voir [profils](#profiles)).

#### <a name="optional-options"></a>Options facultatives
##### <a name="-help"></a>/?, /help
Imprimer l’aide pour `FXC.exe` .

##### <a name="commandoptionfile"></a>@<*commande. option. file*>
Fichier qui contient des options de compilation supplémentaires. Cette option peut être mélangée à d’autres options de compilation de ligne de commande. La *commande. option. file* ne doit contenir qu’une seule option par ligne. La *commande. option. file* ne peut pas contenir de lignes vides. Les options spécifiées dans le fichier ne doivent pas contenir d’espaces de début ou de fin.

##### <a name="all_resources_bound"></a>/all_resources_bound
Activez la mise à plat agressive dans SM 5.1 +. Nouveauté de Direct3D 12.

##### <a name="cc"></a>/CC
Assembly avec code de couleur de sortie.

##### <a name="compress"></a>/compress
Compresser le bytecode de nuanceur facilement à partir de fichiers.

##### <a name="d-idtext"></a>/D <d' *ID* >=< *texte*>
Définissez la macro.

##### <a name="decompress"></a>/decompress
Décompressez le bytecode de nuanceur facilement à partir du premier fichier. Les fichiers de sortie doivent être listés dans l’ordre dans lequel ils se trouvaient lors de la compression.

##### <a name="dumpbin"></a>/dumpbin
Charge un fichier binaire au lieu de compiler un nuanceur.

##### <a name="e-name"></a>/E <name>
Point d’entrée du nuanceur. Si aucun point d’entrée n’est spécifié, **main** est considéré comme le nom de l’entrée du nuanceur.

##### <a name="enable_unbounded_descriptor_tables"></a>/enable_unbounded_descriptor_tables
Active les tables de descripteurs non liées. Nouveauté de Direct3D 12.

##### <a name="extractrootsignature-file"></a>*fichier* de </extractrootsignature>
Extrayez la signature racine à partir du bytecode du nuanceur. Nouveauté de Direct3D 12.

##### <a name="fc-file"></a>/FC <*fichier*>
Fichier de liste de code d’assembly de sortie.

##### <a name="fd-file"></a>*Fichier* </FD>
Extrayez les informations de la base de données du programme Shader (PDB) et écrivez dans le fichier donné. Quand vous compilez le nuanceur, utilisez/FD pour générer un fichier PDB avec les informations de débogage du nuanceur.

##### <a name="fe-file"></a>/Fe <*fichier*>
Affiche les avertissements et les erreurs dans le fichier donné.

##### <a name="fh-file"></a>*Fichier* de </FH>
Fichier d’en-tête de sortie contenant le code objet.

##### <a name="fl-file"></a>*Fichier* de </FL
Sortie d’une bibliothèque. Requiert le \_47.dll D3dcompiler ou une version ultérieure de la dll.

##### <a name="fo-file"></a>/FO <*fichier*>
Fichier objet de sortie. Souvent avec l’extension &quot; . fxc &quot; , bien que d’autres extensions soient utilisées, telles que &quot; . o &quot; , &quot; . obj &quot; ou &quot; . dxbc &quot; .

##### <a name="fx-file"></a>/FX <*fichier*>
Code assembleur de sortie et fichier de liste hexadécimale.

##### <a name="gch"></a>/Gch
Compilez comme un effet enfant pour les profils de fx_4_x.

> [!NOTE]
> La prise en charge des profils d’effets hérités est déconseillée.

##### <a name="gdp"></a>/Gdp
Désactivez le mode performance Effect.

##### <a name="gec"></a>/Gec
Activez le mode de compatibilité descendante.

##### <a name="ges"></a>/Ges
Activez le mode strict.

##### <a name="getprivate-file"></a>*fichier* de </getPrivate>
Enregistrer les données privées à partir de l’objet blob de nuanceur (binaire compilé) dans le fichier donné. Extrait les données privées précédemment incorporées par/SetPrivate à partir de l’objet blob de nuanceur.

Vous devez spécifier l’option/DUMPBIN avec/getPrivate. Par exemple :

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a>/Gfa
Évitez les constructions de contrôle de Flow.

##### <a name="gfp"></a>/GFP
Préférer les constructions de contrôle de Flow.

##### <a name="gis"></a>/Gis
Force la strictité IEEE.

##### <a name="gpp"></a>/Gpp
Forcer une précision partielle.
    
##### <a name="i-include"></a>/I <*include*>
Chemin d’accès include supplémentaire.

##### <a name="lx"></a>/Lx
Littéraux hexadécimaux de sortie. Requiert le \_47.dll D3dcompiler ou une version ultérieure de la dll.

##### <a name="matchuavs"></a>/matchUAVs
Correspond aux allocations de l’emplacement UAV du nuanceur de modèles dans le nuanceur actuel. Pour plus d’informations, consultez la <a href="#remarks">section Notes</a>.

##### <a name="mergeuavs"></a>/mergeUAVs
Fusionner les allocations d’emplacement UAV du nuanceur de modèles et du nuanceur actuel. Pour plus d’informations, consultez la <a href=""></a> <a href="#remarks">section Notes</a>.

##### <a name="ni"></a>/Ni
Numéros d’instruction de sortie dans les listes d’assemblys.

##### <a name="no"></a>/Non
Offset d’octet d’instruction de sortie dans les listes d’assemblys. Quand vous générez un assembly, utilisez/non pour l’annoter avec l’offset d’octet pour chaque instruction.

##### <a name="nologo"></a>/nologo
Supprime le message de copyright.

##### <a name="od"></a>/Od
Désactivez les optimisations. /OD implique/GFP, bien que la sortie ne soit pas identique à/OD/GFP.

##### <a name="op"></a>/Op
Désactiver les prénuanceurs (déconseillé).

##### <a name="o0-o1-o2-o3"></a>/O0/O1,/O2,/O3
Niveaux d’optimisation. O1 est le paramètre par défaut.
- O0 : désactive la réorganisation des instructions. Cela permet de réduire la charge des registres et d’accélérer la simulation de boucle.
- O1 : désactive la réorganisation des instructions pour ps_3_0 et vers le haut.
- O2-identique à O1. Réservé pour un usage futur.
- O3-identique à O1. Réservé pour un usage futur.

##### <a name="p-file"></a>/P <*fichier*>
Prétraiter dans un fichier (doit être utilisé seul).

##### <a name="qstrip_debug"></a>/Qstrip_debug
Supprimez les données de débogage du bytecode de nuanceur pour les profils 4_0 +.

##### <a name="qstrip_priv"></a>/Qstrip_priv
Supprimez les données privées de 4_0 + bytecode de nuanceur. Supprime les données privées (séquence arbitraire d’octets) de l’objet blob de nuanceur (binaire compilé de nuanceur) que vous avez précédemment incorporé avec l' `/setprivate <file>` option.

Vous devez spécifier l’option/DUMPBIN avec/Qstrip_priv. Par exemple :

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a>/Qstrip_reflect
Supprimez les données de réflexion du bytecode de nuanceur pour les profils 4_0 +.

##### <a name="qstrip_rootsignature"></a>/Qstrip_rootsignature
Supprimer la signature racine du bytecode du nuanceur. Nouveauté de Direct3D 12.

##### <a name="res_may_alias"></a>/res_may_alias
Supposons que UAVs/SRVs peut être un alias pour cs_5_0 +. Requiert le \_47.dll D3dcompiler ou une version ultérieure de la dll.

##### <a name="setprivate-file"></a>*fichier* de </SetPrivate>
Ajoutez des données privées dans le fichier donné à l’objet BLOB compilé de nuanceur. Incorpore le fichier donné, qui est traité comme une mémoire tampon brute, à l’objet blob de nuanceur. Utilisez/SetPrivate pour ajouter des données privées quand vous compilez un nuanceur. Vous pouvez également utiliser l’option/DUMPBIN avec/SetPrivate pour charger un objet Shader existant, puis, une fois l’objet en mémoire, ajouter l’objet blob de données privé. Par exemple, utilisez une seule commande avec/SetPrivate pour ajouter des données privées à un objet blob de nuanceur compilé :

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
Ou utilisez deux commandes où la deuxième commande charge un objet Shader, puis ajoute des données privées :

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a>*fichier* de </setrootsignature>
Attachez la signature racine au bytecode du nuanceur. Nouveauté de Direct3D 12.

##### <a name="shtemplate-file"></a>*fichier* de </shtemplate>
Utilisez le fichier de nuanceur de modèle donné pour la fusion (/mergeUAVs) et les ressources (/matchUAVs) correspondantes. Pour plus d’informations, consultez la <a href="#remarks">section Notes</a>.

##### <a name="vd"></a>/VD
Désactivez la validation.

##### <a name="verifyrootsignature-file"></a>*fichier* de </verifyrootsignature>
Vérifiez le bytecode du nuanceur par rapport à la signature racine. Nouveauté de Direct3D 12.

##### <a name="vi"></a>/Vi
Affichez des détails sur le processus d’inclusion.

##### <a name="vn-name"></a>*Nom* de l' </VN>
Utilisez nom comme nom de variable dans le fichier d’en-tête.

##### <a name="wx"></a>/WX
Considérer les avertissements comme des erreurs.

##### <a name="zi"></a>/Zi
Activez les informations de débogage.

##### <a name="zpc"></a>/Zpc
Compresser les matrices dans l’ordre des colonnes.

##### <a name="zpr"></a>/Zpr
Compresser les matrices dans l’ordre ligne-principal.

### <a name="filenames"></a>*Noms de fichiers*

\[dans \] les fichiers qui contiennent le ou les nuanceurs et/ou les effets.

## <a name="remarks"></a>Notes

Utilisez les `/mergeUAVs` `/matchUAVs` options, et `/shtemplate` pour aligner les emplacements de liaison UAV pour une chaîne de nuanceurs.

Supposons que vous avez des nuanceurs A. FX, B. FX et C. fx. Pour aligner les emplacements de liaison UAV pour cette chaîne de nuanceurs, vous avez besoin de deux passes de compilation :

**Pour aligner les emplacements de liaison UAV pour une chaîne de nuanceurs**

1.  Utilisez/mergeUAVs pour compiler des nuanceurs et spécifiez un objet blob de nuanceur compilé précédemment avec/shtemplate. Par exemple :
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  Utilisez/matchUAVs pour compiler des nuanceurs et spécifiez le dernier objet blob de nuanceur de la première passe avec/shtemplate. Vous pouvez compiler dans n’importe quel ordre. Par exemple :
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
Vous n’avez pas besoin de recompiler C. fx dans la deuxième passe.

Après avoir effectué les deux réussites de compilation précédentes, vous pouvez utiliser A. o, B. o et C. o comme objets BLOB de nuanceur finaux avec des emplacements UAV alignés.

## <a name="profiles"></a>Profils

Chaque modèle de nuanceur est étiqueté avec un profil HLSL. Pour compiler un nuanceur par rapport à un modèle de nuanceur particulier, choisissez le profil de nuanceur approprié dans le tableau suivant.

<table><thead><tr class="header"><th>Type de nuanceur</th><th>Profils</th></tr></thead><tbody><tr class="odd"><td>Nuanceur de calcul</td><td><dl> cs_4_0<br />
cs_4_1<br />
cs_5_0<br />
cs_5_1<br />
</dl></td></tr><tr class="even"><td>Nuanceur de domaine</td><td><dl> ds_5_0<br />
ds_5_1<br />
</dl></td></tr><tr class="odd"><td>Nuanceur de géométrie</td><td><dl> gs_4_0<br />
gs_4_1<br />
gs_5_0<br />
gs_5_1<br />
</dl></td></tr><tr class="even"><td>Liaison de nuanceur HLSL </td><td><dl> lib_4_0<br />
lib_4_1<br />
lib_4_0_level_9_1<br />
lib_4_0_level_9_1_vs_only<br />
lib_4_0_level_9_1_ps_only<br />
lib_4_0_level_9_3<br />
lib_4_0_level_9_3_vs_only<br />
lib_4_0_level_9_3_ps_only<br />
lib_5_0<br />
</dl> Pour plus d’informations sur la liaison de nuanceur, consultez <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> et <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>. <br/></td></tr><tr class="odd"><td>Nuanceur de coque</td><td><dl> hs_5_0<br />
hs_5_1<br />
</dl></td></tr><tr class="even"><td>Nuanceur de pixels</td><td><dl> ps_2_0<br />
ps_2_a<br />
ps_2_b<br />
ps_2_sw<br />
ps_3_0<br />
ps_3_sw<br />
ps_4_0<br />
ps_4_0_level_9_0<br />
ps_4_0_level_9_1<br />
ps_4_0_level_9_3<br />
ps_4_1<br />
ps_5_0<br />
ps_5_1<br />
</dl></td></tr><tr class="odd"><td>Signature racine</td><td><dl> rootsig_1_0<br />
</dl></td></tr><tr class="even"><td>Nuanceur de texture</td><td><dl> tx_1_0<br />
</dl></td></tr><tr class="odd"><td>Nuanceur de sommets</td><td><dl> vs_1_1<br />
vs_2_0<br />
vs_2_a<br />
vs_2_sw<br />
vs_3_0<br />
vs_3_sw<br />
vs_4_0<br />
vs_4_0_level_9_0<br />
vs_4_0_level_9_1<br />
vs_4_0_level_9_3<br />
vs_4_1<br />
vs_5_0<br />
vs_5_1<br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a>Notes de version

Pour Direct3D 12, consultez [spécification de signatures racines en langage HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [liaison de ressources en HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) et [indexation dynamique à l’aide de HLSL 5,1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).

Dans Direct3D 10, utilisez l’API pour obtenir le sommet, la géométrie et le profil de nuanceur de pixels qui conviennent le mieux à un appareil donné en appelant les fonctions suivantes : [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)et [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).

Dans Direct3D 9, utilisez les méthodes [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) ou [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) pour récupérer les profils vertex et de nuanceur de pixels pris en charge par un appareil. La structure [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) retournée par ces méthodes indique les profils vertex et de nuanceur de pixels pris en charge par un appareil dans ses membres **VertexShaderVersion** et **PixelShaderVersion** .

Pour obtenir des exemples, consultez [compilation avec le compilateur actuel](dx-graphics-tools-fxc-using.md).

## <a name="related-topics"></a>Rubriques connexes

* [Effect-Tool du compilateur](fxc.md)