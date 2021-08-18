---
description: empêche une entrée de menu Démarrer pour un raccourci d’application récemment installé de recevoir une surbrillance.
ms.assetid: ff85da6f-a506-4225-8ac9-4a8a7be8d599
title: System. AppUserModel. ExcludeFromShowInNewInstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba75b28b789fd9972eb484797957601dbcb5e93694b469eeb8b81bf9ba198d13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970898"
---
# <a name="systemappusermodelexcludefromshowinnewinstall"></a>System. AppUserModel. ExcludeFromShowInNewInstall

Empêche une entrée de menu **Démarrer** pour un raccourci d’application récemment installé de recevoir une surbrillance. Cela revient à désactiver l’option **mettre en surbrillance les programmes récemment installés** dans la fenêtre **personnaliser le menu Démarrer** sur un élément individuel. Cette propriété doit être définie sur les raccourcis pour les outils et les applications secondaires.

> [!Note]  
> cette propriété est utilisée uniquement par le menu Démarrer sur Windows Vista et Windows 7. la propriété n’est pas utilisée par l’écran de démarrage ou menu Démarrer sur Windows 8 et versions ultérieures

 

.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.ExcludeFromShowInNewInstall
   shellPKey = PKEY_AppUserModel_ExcludeFromShowInNewInstall
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a>Remarques

Les valeurs de la valeur de l’une sont définies dans propKey. h.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md)
</dt> <dt>

[System.AppUserModel.ID](./props-system-appusermodel-id.md)
</dt> <dt>

[**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[aliasInfo](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[variables](./propdesc-schema-enum.md)
</dt> <dt>

[enumRange](./propdesc-schema-enumrange.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[relatedProperty](./propdesc-schema-relatedproperty.md)
</dt> <dt>

[startPinOption](/previous-versions//jj553605(v=vs.85))
</dt> </dl>

 

 
