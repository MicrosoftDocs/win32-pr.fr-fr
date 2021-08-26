---
description: La méthode DVDAdm. ChangePassword enregistre un nouveau mot de passe d’application dans le registre.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: ChangePassword, méthode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f5d15eef943afa019f1b1bba4e3b1412978bc5dd8f52f411c504e880428848a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999329"
---
# <a name="changepassword-method"></a>ChangePassword, méthode

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.ChangePassword` méthode enregistre un nouveau mot de passe d’application dans le registre.

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Spécifie le nom d’ouverture de session de l’utilisateur actuel en tant que chaîne. L’objet MSDVDAdm ignore ce paramètre. Consultez la section Notes.

</dd> <dt>

<span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Vendus*
</dt> <dd>

Spécifie l’ancien mot de passe de l’utilisateur sous la forme d’une chaîne.

</dd> <dt>

<span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*
</dt> <dd>

Spécifie le nouveau mot de passe de l’utilisateur sous la forme d’une chaîne. ne peut pas être une chaîne vide.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Actuellement, le paramètre *sUserName* est ignoré sur cette et toutes les méthodes associées. Cela signifie que toute personne connaissant le mot de passe peut définir le niveau parental. Il n’existe qu’un seul mot de passe et un seul niveau parental pour l’application. Il n’existe aucune prise en charge pour les noms d’ouverture de session des utilisateurs individuels ou la gestion de plusieurs mots de passe. Pour appliquer des niveaux de gestion parental, les parents doivent définir le mot de passe, puis définir le niveau parental approprié pour les jeunes membres du groupe de parents. Lorsque les parents souhaitent afficher un disque avec un contenu classé pour adultes, ils peuvent modifier le niveau, puis le modifier à la fin de l’affichage. Tant que les enfants ne connaissent pas le mot de passe, ils peuvent uniquement regarder le contenu au niveau ou au-dessous du niveau défini pour eux.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ConfirmPassword**](confirmpassword-method.md)
</dt> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



