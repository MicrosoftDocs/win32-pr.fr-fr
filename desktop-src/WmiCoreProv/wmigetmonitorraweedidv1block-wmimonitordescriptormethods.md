---
description: Obtient les données brutes pour une structure E-EDID (Enhanced Display standard Association) améliorée de la norme VESA (Video Electronics Association) qui définit des paramètres optimaux pour la configuration d’une analyse.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: Méthode WmiGetMonitorRawEEdidV1Block de la classe WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1af1ddb86a90ea9029d5cba408745fe3dafa69dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533674"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a>Méthode WmiGetMonitorRawEEdidV1Block de la classe WmiMonitorDescriptorMethods

La méthode **WmiGetMonitorRawEEdidV1Block** obtient les données brutes pour une structure de données d’identification d’affichage étendu (E-EDID) améliorée d’association Video Electronics standard Association (VESA) qui définit des paramètres optimaux pour la configuration d’une analyse.

## <a name="syntax"></a>Syntaxe


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*BlockId* \[ dans\]
</dt> <dd>

Identité du bloc de données.

</dd> <dt>

*BlockType* \[ à\]
</dt> <dd>

Type de bloc de données. Le tableau suivant répertorie les valeurs de retour possibles.



| Valeur                                                                                 | Signification                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>    | Non initialisé(e)<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | Bloc de base EDID<br/> |
| <dl> <dt>2 (0X2)</dt> </dl>    | Carte de blocs EDID<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Autres<br/>           |



 

</dd> <dt>

*BlockContent* \[ à\]
</dt> <dd>

Tableau de 128 octets qui contient le contenu du bloc brut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro (0) pour indiquer la réussite de l’opération. Tout autre nombre indique une erreur. Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="examples"></a>Exemples

L’exemple de code suivant récupère les blocs EDID de n’importe quel affichage sous la forme de tableaux 128 bits bruts.


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Espace de noms<br/>                | \\WMI racine<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

