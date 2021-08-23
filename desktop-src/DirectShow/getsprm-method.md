---
description: La méthode GetSPRM récupère le registre de paramètres système spécifié.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Méthode GetSPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e254d23f0d70890516bc5655f6c4ea38133a8a3733360955cabf9040207f3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536989"
---
# <a name="getsprm-method"></a>Méthode GetSPRM

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetSPRM` méthode récupère le registre de paramètres système spécifié.

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Spécifie l’enregistrement dont vous souhaitez récupérer la valeur sous la forme d’un entier. L’entier doit être compris entre 0 et 23.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le contenu du Registre spécifié.

## <a name="remarks"></a>Remarques

Le disque contrôle les registres des paramètres système (SPRMs). Une application de lecteur n’A pas besoin d’accéder à ces registres pour les fonctionnalités de navigation standard. SPRMs représente l’état du joueur. Chacune d’elles a une signification, définie par les préférences de l’utilisateur, les commandes de disque et d’autres occurrences qu’une application n’a pas de contrôle direct. Une application peut lire ces registres, mais ne peut pas y écrire. Pour utiliser ces registres efficacement, vous aurez probablement besoin d’une connaissance plus détaillée des commandes de navigation de DVD que celles fournies dans cette documentation. Le tableau suivant présente le contenu de chaque registre. Pour plus d’informations sur le contenu du Registre, consultez [ **IDvdInfo2 :: GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)



| S’inscrire | Contenu                        |
|----------|---------------------------------|
| 0        | Code de la langue du menu              |
| 1        | Numéro de flux audio             |
| 2        | Numéro de flux de sous-image        |
| 3        | Nombre actuel d’angles            |
| 4        | Numéro de titre actuel            |
| 5        | Numéro de titre                    |
| 6        | Nombre de PGC                      |
| 7        | Numéro du chapitre actuel (PTT)    |
| 8        | Numéro du bouton mis en surbrillance       |
| 9        | Minuteur de navigation                |
| 10       | Jump pour le point de vue de la navigation. minuterie (Timer)         |
| 11       | Mode de présentation audio karaoké |
| 12       | Code pays/région PML         |
| 13       | PML                             |
| 14       | Paramètre vidéo                   |
| 15       | Fonctionnalité audio                |
| 16       | Langue audio                  |
| 17       | Extension de langage audio        |
| 18       | Langue de la sous-image             |
| 19       | Extension du langage de sous-image   |
| 20       | Code de la région du joueur              |
| 21       | Réservé                        |
| 22       | Réservé                        |
| 23       | Réservé                        |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetGPRM**](getgprm-method.md)
</dt> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



