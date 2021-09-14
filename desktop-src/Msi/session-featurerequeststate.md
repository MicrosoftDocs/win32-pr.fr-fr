---
description: La propriété FeatureRequestState est une propriété en lecture-écriture de l’objet session.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Session. FeatureRequestState, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007320"
---
# <a name="sessionfeaturerequeststate-property"></a>Session. FeatureRequestState, propriété

La propriété **FeatureRequestState** est une propriété en lecture-écriture de l’objet [**session**](session-object.md) . Il peut être utilisé pour obtenir l’état d’action actuel d’une fonctionnalité ou pour demander une modification de l’action d’une fonctionnalité et de ses sous-composants. La fonctionnalité doit être nommée dans le tableau des [fonctionnalités](feature-table.md) . Si une modification de l’état d’action d’une fonctionnalité est demandée, l’état d’action de tous les composants de la fonctionnalité modifiée peut également être modifié. L’état d’action des composants partagés par plusieurs fonctionnalités sera modifié en fonction du nouvel état de l’action de fonctionnalité (consultez la section Notes). La propriété **FeatureRequestState** peut également être utilisée pour configurer toutes les fonctionnalités à la fois en spécifiant le mot clé All à la place d’un nom de fonctionnalité spécifique.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne obligatoire qui spécifie le nom de la fonctionnalité à configurer. Pour définir l’état de la demande de toutes les fonctionnalités, utilisez le mot réservé ne respectant pas la casse : ALL.

## <a name="remarks"></a>Notes

La méthode [**SetInstallLevel**](session-setinstalllevel.md) doit être appelée avant d’appeler **FeatureRequestState**.

Si l’état actuel de la fonctionnalité est demandé, la propriété **FeatureRequestState** retourne l’une des valeurs suivantes.



| Nom de l’état de sélection         | Signification                                                               |
|------------------------------|-----------------------------------------------------------------------|
| msiInstallStateUnknown =-1  | Aucune action n’est effectuée pour la fonctionnalité. Cela équivaut à la valeur null.       |
| msiInstallStateAdvertised = 1 | La fonctionnalité doit être publiée.                                          |
| msiInstallStateAbsent = 2    | La fonctionnalité doit être supprimée.                                             |
| msiInstallStateLocal = 3     | La fonctionnalité doit être installée en tant qu’exécution locale.                              |
| msiInstallStateSource = 4    | La fonctionnalité doit être installée en tant qu’exécution à partir de la source.                        |
| msiInstallStateDefault = 5   | La fonctionnalité doit être réinstallée avec l’état d’action actuel de la fonctionnalité. |



 

Par exemple, le code suivant obtient l’état actuel de « MyFeature » à partir d’une action personnalisée VBScript.


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



Si l’état de la fonctionnalité est configuré, la propriété **FeatureRequestState** doit être définie sur l’une des valeurs suivantes.



| Nom de l’état de sélection          | Signification                                 |
|-------------------------------|-----------------------------------------|
| msiInstallStateAdvertised = 1 | Publiez la fonctionnalité.                  |
| msiInstallStateAbsent = 2     | Supprimez la fonctionnalité.                     |
| msiInstallStateLocal = 3      | Installez la fonctionnalité en tant qu’exécution locale.       |
| msiInstallStateSource = 4     | Installez la fonctionnalité en tant qu’exécution à partir de la source. |



 

Par exemple, les requêtes suivantes d’une action personnalisée VBScript que « MyFeature » sont installées pour s’exécuter localement sur l’ordinateur.


```VB
Session.FeatureRequestState("MyFeature")=3
```



Quand **FeatureRequestState** est appelé, le programme d’installation tente de définir l’état d’action de chaque composant lié à la fonctionnalité spécifiée à l’état spécifié, le plus possible. Toutefois, il existe des situations courantes dans lesquelles la demande ne peut pas être entièrement honorée. Par exemple, si une fonctionnalité est liée à deux composants, le composant A et le composant B, via la table [FeatureComponents](featurecomponents-table.md) et le composant a, l’attribut **msidbComponentAttributesLocalOnly** et le composant b ont l’attribut **msidbComponentAttributesSourceOnly** . Dans ce cas, si **FeatureRequestState** est appelé avec l’État demandé MsiInstallStateLocal ou msiInstallStateSource, la requête ne peut pas être honorée pour les deux composants. Dans ce cas, les deux composants peuvent être activés avec le composant A défini sur msiInstallStateLocal et le composant B défini sur msiInstallStateSource.

Si plusieurs fonctionnalités sont liées à un seul composant, l’état d’action final de ce composant est déterminé comme suit : si au moins une fonctionnalité exige que le composant soit installé localement, il est installé msiInstallStateLocal. Si au moins une fonctionnalité exige que le composant soit exécuté à partir du média source, il est installé msiInstallStateSource. Si au moins une fonctionnalité appelle pour la suppression du composant, l’état d’action est msiInstallStateAbsent. Pour plus d’informations sur la sélection des fonctionnalités pour l’installation, [consultez le tableau des fonctionnalités.](feature-table.md)

Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**session**](session-object.md)
</dt> <dt>

[Fonctionnalité](feature-table.md)
</dt> </dl>

 

 




