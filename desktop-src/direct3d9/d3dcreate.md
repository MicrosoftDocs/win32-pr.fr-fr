---
description: Consultez une combinaison d’un ou plusieurs indicateurs qui contrôlent le comportement de création de l’appareil dans la constante D3DCREATE.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c24529c725b8b7c7f71c53718d56ceb50603
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011282"
---
# <a name="d3dcreate"></a>D3DCREATE

Combinaison d’un ou de plusieurs indicateurs qui contrôlent le comportement de création de l’appareil.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#définition</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DCREATE_ADAPTERGROUP_DEVICE</td>
<td>L’application demande à l’appareil de piloter tous les en-têtes détenus par cet adaptateur maître. L’indicateur n’est pas conforme sur les adaptateurs non maîtres. Si cet indicateur est défini, les paramètres de présentation passés à <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> doivent pointer vers un tableau de <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>. Le nombre d’éléments dans <strong>D3DPRESENT_PARAMETERS</strong> doit être égal au nombre d’adaptateurs défini par le membre NumberOfAdaptersInGroup de la structure <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> . Le runtime DirectX assignera chaque élément à chaque tête dans l’ordre numérique spécifié par le membre AdapterOrdinalInGroup de <strong>D3DCAPS9</strong>.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT</td>
<td>Direct3D gérera les ressources au lieu du pilote. Les appels Direct3D n’échoueront pas pour les erreurs de ressources telles que la mémoire vidéo insuffisante.</td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</td>
<td>Comme D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D gère les ressources au lieu du pilote. Contrairement à D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX renvoie des erreurs pour des conditions telles qu’une mémoire vidéo insuffisante.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_PRINTSCREEN</td>
<td>Le runtime n’enregistre pas les touches d’accès rapide pour printscreen, Ctrl-Printscreen et Alt-Printscreen pour capturer le contenu du bureau ou de la fenêtre. 
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_PSGP_THREADING</td>
<td>Limitez le calcul au thread d’application principal. Si l’indicateur n’est pas défini, le runtime peut effectuer le traitement du vertex logiciel et d’autres calculs dans le thread de travail afin d’améliorer les performances sur les systèmes multiprocesseurs. 
<table>
<tbody>
<tr class="odd">
<td>Différences entre Windows XP et Windows Vista :<br/> Cet indicateur est disponible sur Windows Vista, Windows Server 2008 et Windows 7.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DCREATE_ENABLE_PRESENTSTATS</td>
<td>Active la collecte des statistiques actuelles sur l’appareil. Les appels à <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> retournent des données valides. 
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_FPU_PRESERVE</td>
<td>Définissez la précision des calculs en virgule flottante Direct3D sur la précision utilisée par le thread appelant. Si vous ne spécifiez pas cet indicateur, Direct3D passe par défaut au mode d’aller-à-proche simple précision pour deux raisons :
<ul>
<li>Le mode double précision réduit les performances Direct3D.</li>
<li>Des portions de Direct3D supposent que les exceptions d’unité à virgule flottante sont masquées ; le démasquage de ces exceptions peut entraîner un comportement indéfini.</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCREATE_HARDWARE_VERTEXPROCESSING</td>
<td>Spécifie le traitement du vertex matériel.</td>
</tr>
<tr class="even">
<td>D3DCREATE_MIXED_VERTEXPROCESSING</td>
<td>Spécifie le traitement des vertex mixtes (logiciels et matériels). Pour Windows 10, version 1607 et versions ultérieures, l’utilisation de ce paramètre n’est pas recommandée. Consultez D3DCREATE_SOFTWARE_VERTEXPROCESSING.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SOFTWARE_VERTEXPROCESSING</td>
<td>Spécifie le traitement du vertex logiciel. Pour Windows 10, version 1607 et versions ultérieures, l’utilisation de ce paramètre n’est pas recommandée. Utilisez D3DCREATE_HARDWARE_VERTEXPROCESSING.
<div class="alert">
<blockquote>
[!Note]<br />
Sauf si le traitement du vertex matériel n’est pas disponible, l’utilisation du traitement du vertex logiciel n’est pas recommandée dans Windows 10, version 1607 (et versions ultérieures), car l’efficacité du traitement du vertex logiciel a été considérablement réduite, tout en améliorant la sécurité de l’implémentation.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_MULTITHREADED</td>
<td>Indique que l’application demande à Direct3D d’être de sécurité multithread. Cela permet à un thread Direct3D de prendre possession de sa <a href="/windows/desktop/Sync/critical-section-objects">section critique</a> globale plus fréquemment, ce qui peut dégrader les performances. Si une application traite des messages de fenêtre dans un thread lors de l’exécution d’appels d’API Direct3D dans un autre, l’application doit utiliser cet indicateur lors de la création de l’appareil. Cette fenêtre doit également être détruite avant de décharger d3d9.dll.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_NOWINDOWCHANGES</td>
<td>Indique que Direct3D ne doit pas modifier la fenêtre de focus de quelque manière que ce soit.
<div class="alert">
<blockquote>
[!Note]<br />
Si cet indicateur est défini, l’application doit prendre entièrement en charge tous les événements de gestion de focus, tels que ALT + TAB et les événements de clic de souris.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_PUREDEVICE</td>
<td>Spécifie que Direct3D ne prend pas en charge les appels d’extraction * pour tout ce qui peut être stocké dans des blocs d’État. Il indique également à Direct3D de ne pas fournir de services d’émulation pour le traitement des vertex. Cela signifie que si l’appareil ne prend pas en charge le traitement des vertex, l’application ne peut utiliser que des sommets convertis.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SCREENSAVER</td>
<td>Permet d’obtenir des économiseurs d’écran pendant une application en plein écran. Sans cet indicateur, Direct3D désactivera les économiseurs d’écran tant que l’application appelante est en plein écran. Si l’application appelante est déjà un économiseur d’écran, cet indicateur n’a aucun effet. 
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

\_Les D3DCREATE matériels \_ VERTEXPROCESSING, D3DCREATE \_ Mixed \_ VERTEXPROCESSING et D3DCREATE \_ Software \_ VERTEXPROCESSING sont des indicateurs mutuellement exclusifs. Au moins un de ces indicateurs de traitement de vertex doit être spécifié lors de l’appel de [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).

## <a name="constant-information"></a>Informations constantes



| Condition requise                         |  Valeur          |
|--------------------------|------------|
| En-tête                   | D3D9. h     |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
