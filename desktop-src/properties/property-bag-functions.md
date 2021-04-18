---
description: Cette section décrit un ensemble de fonctions d’assistance Windows utilisées avec les objets IPropertyBag.
ms.assetid: 4ef85855-7eb6-43ec-bf29-1223eaf1a0cc
title: Fonctions de jeu de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c86a2e3ce61805702641f893d51f5c4aa26b0ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536168"
---
# <a name="property-bag-functions"></a>Fonctions de jeu de propriétés

Cette section décrit un ensemble de fonctions d’assistance Windows utilisées avec les objets [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) .



| Rubrique                                                                       | Contenu                                                                                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PSPropertyBag \_ Supprimer**](/windows/win32/api/propsys/nf-propsys-pspropertybag_delete)                     | Supprime une propriété d’un conteneur de propriétés.<br/>                                                                           |
| [**PSPropertyBag \_ ReadBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbool)                 | Lit la valeur de données **bool** d’une propriété dans un conteneur de propriétés.<br/>                                                    |
| [**PSPropertyBag \_ ReadBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbstr)                 | Lit une valeur de données **BSTR** à partir d’une propriété dans un conteneur de propriétés.<br/>                                                    |
| [**PSPropertyBag \_ ReadDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readdword)               | Lit une valeur de données **DWORD** à partir de la propriété dans un conteneur de propriétés.<br/>                                                     |
| [**PSPropertyBag \_ ReadGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readguid)                 | Lit la valeur de données de GUID d’une propriété dans un conteneur de propriétés.<br/>                                                      |
| [**PSPropertyBag \_ ReadInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readint)                   | Lit une valeur de données **int** à partir d’une propriété dans un conteneur de propriétés.<br/>                                                    |
| [**PSPropertyBag \_ ReadLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readlong)                 | Lit une valeur de données de **type long** à partir d’une propriété dans un conteneur de propriétés.<br/>                                                    |
| [**PSPropertyBag \_ ReadPOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpointl)             | Récupère les coordonnées de propriété stockées dans une structure [**pointe**](/previous-versions//dd162807(v=vs.85)) d’un conteneur de propriétés spécifié.<br/>    |
| [**PSPropertyBag \_ ReadPOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpoints)             | Récupère les coordonnées de propriété stockées dans une structure de [**points**](/previous-versions//dd162808(v=vs.85)) d’un conteneur de propriétés spécifié.<br/>    |
| [**PSPropertyBag \_ ReadPropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpropertykey)   | Lit la clé de propriété d’une propriété dans un conteneur de propriétés spécifié.<br/>                                                 |
| [**PSPropertyBag \_ ReadRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readrectl)               | Récupère les coordonnées d’un rectangle stocké dans une propriété contenue dans un conteneur de propriétés spécifié.<br/>              |
| [**PSPropertyBag \_ ReadSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readshort)               | Lit la valeur de données **courtes** d’une propriété dans un conteneur de propriétés.<br/>                                                   |
| [**PSPropertyBag \_ ReadStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstr)                   | Lit la valeur de données de **chaîne** d’une propriété dans un conteneur de propriétés.<br/>                                                  |
| [**PSPropertyBag \_ ReadStrAlloc**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstralloc)         | Lit une valeur de données de **type chaîne** à partir d’une propriété dans un conteneur de propriétés et alloue de la mémoire pour la chaîne lue.<br/> |
| [**PSPropertyBag \_ ReadStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstream)             | Lit le flux de données stocké dans une propriété donnée contenue dans un conteneur de propriétés spécifié.<br/>                           |
| [**PSPropertyBag \_ ReadType**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readtype)                 | Lit le type de la valeur de données d’une propriété qui est stockée dans un conteneur de propriétés.<br/>                                      |
| [**PSPropertyBag \_ ReadULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readulonglong)       | Lit une valeur de données **ULONGLONG** à partir d’une propriété dans un conteneur de propriétés.<br/>                                               |
| [**PSPropertyBag \_ ReadUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readunknown)           | Lit une propriété donnée d’une valeur de données inconnue dans un conteneur de propriétés.<br/>                                                |
| [**PSPropertyBag \_ WriteBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebool)               | Définit la valeur de données **bool** d’une propriété dans un conteneur de propriétés.<br/>                                                     |
| [**PSPropertyBag \_ WriteBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebstr)               | Définit une valeur de données **BSTR** à partir d’une propriété dans un conteneur de propriétés.<br/>                                                     |
| [**PSPropertyBag \_ WriteDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writedword)             | Définit une valeur de données **DWORD** à partir de la propriété dans un conteneur de propriétés.<br/>                                                      |
| [**PSPropertyBag \_ WriteGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeguid)               | Définit la valeur de données de GUID à partir d’une propriété dans un conteneur de propriétés.<br/>                                                       |
| [**PSPropertyBag \_ writeInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeint)                 | Définit une valeur de données **int** à partir d’une propriété dans un conteneur de propriétés.<br/>                                                     |
| [**PSPropertyBag \_ WriteLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writelong)               | Définit une valeur de données de **type long** à partir d’une propriété dans un conteneur de propriétés.<br/>                                                     |
| [**PSPropertyBag \_ WritePOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepointl)           | Stocke les coordonnées de propriété stockées dans une structure [**pointe**](/previous-versions//dd162807(v=vs.85)) d’un conteneur de propriétés spécifié.<br/>       |
| [**PSPropertyBag \_ WritePOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepoints)           | Stocke les coordonnées de propriété stockées dans une structure de [**points**](/previous-versions//dd162808(v=vs.85)) d’un conteneur de propriétés spécifié.<br/>       |
| [**PSPropertyBag \_ WritePropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepropertykey) | Définit la clé de propriété d’une propriété dans un conteneur de propriétés spécifié.<br/>                                                  |
| [**PSPropertyBag \_ WriteRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writerectl)             | Stocke les coordonnées d’un rectangle stocké dans une propriété contenue dans un conteneur de propriétés spécifié.<br/>                 |
| [**PSPropertyBag \_ WriteSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeshort)             | Définit la valeur de données **courtes** d’une propriété dans un conteneur de propriétés.<br/>                                                    |
| [**PSPropertyBag \_ WriteStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestr)                 | Définit la valeur de données de **chaîne** d’une propriété dans un conteneur de propriétés.<br/>                                                   |
| [**PSPropertyBag \_ WriteStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestream)           | Définit le flux de données stocké dans une propriété donnée contenue dans un conteneur de propriétés spécifié.<br/>                            |
| [**PSPropertyBag \_ WriteULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeulonglong)     | Définit une valeur de données **ULONGLONG** à partir d’une propriété dans un conteneur de propriétés.<br/>                                                |
| [**PSPropertyBag \_ WriteUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeunknown)         | Définit une propriété donnée d’une valeur de données inconnue dans un conteneur de propriétés.<br/>                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions PROPVARIANT et VARIANT](./functions-propvarutil.md)
</dt> <dt>

[Fonctions](functions.md)
</dt> </dl>

 

 
