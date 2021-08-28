---
description: 'En savoir plus sur : structure JET_SPACEHINTS'
title: Structure JET_SPACEHINTS
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77c452fb78916fdcdf935ec6ad890db055e63b9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479315"
---
# <a name="jet_spacehints-structure"></a>Structure JET_SPACEHINTS


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_spacehints-structure"></a>Structure JET_SPACEHINTS

La structure **JET_SPACEHINTS** contient des informations sur les modèles d’allocation d’espace quand une arborescence binaire (b-Tree) s’agrandit via les fractionnements Append ou Hotpoint. Les fractionnements d’ajout se produisent lorsque des enregistrements sont ajoutés à la fin d’un arbre b (b-Tree) et que des fractionnements Hotpoint se produisent lorsque plusieurs enregistrements sont ajoutés au même point d’insertion virtuel (par exemple, en ajoutant « Marie », « Mark », « Martin' », « Mary » au milieu d’une arborescence binaire qui est triée par ordre alphabétique).

**Windows 7 :** la structure **JET_SPACEHINTS** est introduite dans Windows 7.

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a>Membres

**cbStruct**

Taille, en octets, de cette structure. Affectez à ce membre la valeur sizeof (JET_SPACEHINTS).

**ulInitialDensity**

La densité au format (Append).

**cbInitial**

Taille initiale (en octets) de l’objet en cours de création. Il doit s’agir d’un multiple de la taille de page de la base de données.

**grbit**

Groupe de bits qui contient les options à utiliser pour cette structure, qui incluent zéro ou plusieurs des éléments suivants.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitSpaceHintsUtilizeParentSpace<br />0x00000001</p> | <p>Modifie la stratégie d’allocation interne pour obtenir l’espace heirarchically à partir du parent immédiat d’une arborescence binaire (b-Tree).</p> | 
| <p>JET_bitCreateHintAppendSequential<br />0x00000002</p> | <p>Active le comportement de fractionnement d’ajout pour augmenter en fonction de la dynamique de croissance de la table (définie par cbMinExtent, ulGrowth, cbMaxExtent).</p> | 
| <p>JET_bitCreateHintHotpointSequential<br />0x00000004</p> | <p>Active le comportement de fractionnement Hotpoint pour augmenter en fonction de la dynamique de croissance de la table (définie par cbMinExtent, ulGrowth, cbMaxExtent).</p> | 
| <p>JET_bitRetrieveHintTableScanForward<br />0x00000010</p> | <p>Si cette valeur est définie, le client indique que l’analyse par progression séquentielle est le modèle d’utilisation prédominant de ce tableau.</p> | 
| <p>JET_bitRetrieveHintTableScanBackward<br />0x00000020</p> | <p>Si cette valeur est définie, le client indique que l’analyse de séquence arrière est le modèle d’utilisation prédominant de cette table.</p> | 
| <p>JET_bitDeleteHintTableSequential<br />0x00000100</p> | <p>Si cette valeur est définie, l’application s’attend à ce que cette table soit nettoyée dans l’ordre séquentiel, de la clé la plus basse à la clé la plus élevée.</p> | 



**ulMaintDensity**

densité à mulMaintDensity

Densité à gérer à. Si les indicateurs d’espace spécifient JET_bitRetrieveHintTableScanForward ou JET_bitRetrieveHintTableScanBackward, la défragmentation de table est déclenchée lorsque l’espace utilisé dans le tableau chute sous ce seuil. La défragmentation de table peut être désactivée en affectant à ce membre la valeur zéro. La définition de ce membre sur 100 entraînera l’exécution de la défragmentation de la table dès qu’une page sera libérée.

**ulGrowth**

Croissance en pourcentage de la dernière croissance ou taille initiale, arrondie à la taille d’allocation JET Native la plus proche.

**cbMinExtent trop petit**

Cela remplace ulGrowth s’il est trop petit.

**cbMaxExtent**

Valeur maximale pour la croissance en octets. Ce cap ulGrowth.

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>Quand une arborescence binaire (b-Tree) croît par le biais d’ajouts ou de fractionnements Hotpoint (par opposition aux insertions d’enregistrements aléatoires), la quantité d’espace que la table augmentera est calculée comme suit :

1.  Lors de la création, nous offrons toujours le cbInitial d’arbre b (b-Tree).

2.  Lors de la première allocation d’une zone donnée, nous allons allouer : cbInitial \* ulGrowth/100 (arrondi à la taille de page de la base de données) ou cbMinExtent s’il est plus grand.

3.  Lors de la prochaine allocation, cbLastAlloc \* ulGrowth/100 (arrondi à la taille de page de la base de la base de la base de la base de la base) ou cbMinExtent s’il est plus grand.

4.  À une certaine allocation (qui peut être la première allocation), la taille calculée dépassera cbMaxExtent et sera la taille de croissance par la suite.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
