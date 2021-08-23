---
title: considérations relatives à la Stockage de propriétés
description: IPropertyStorage ReadMultiple lit autant de propriétés spécifiées dans le tableau rgpspec que dans le jeu de propriétés.
ms.assetid: 7540966f-a3b2-46c9-9e04-b15133a517eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128c5da70ae08c62660e0177187036fddee6ff27ed1d9971b6f95dea7052ecdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662159"
---
# <a name="property-storage-considerations"></a>considérations relatives à la Stockage de propriétés

[**IPropertyStorage :: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) lit autant de propriétés spécifiées dans le tableau *rgpspec* que dans le jeu de propriétés. Tant que l’une des propriétés demandées est lue, une demande de récupération d’une propriété qui n’existe pas n’est pas une erreur. Au lieu de cela, elle doit entraîner \_ l’écriture de VT vide pour cette propriété dans le tableau *rgvar* \[ \] lors du retour. Si aucune des propriétés demandées n’existe, la méthode doit retourner S \_ false et définir VT \_ vide dans chaque [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Si une autre erreur est retournée, aucune valeur de propriété n’est récupérée et l’appelant n’a pas besoin de se préoccuper de la libération.

Le paramètre *rgpspec* est un tableau de structures [**PROPSPEC**](/windows/win32/api/propidlbase/ns-propidlbase-propspec) , qui spécifient pour chaque propriété son identificateur de propriété ou, le cas échéant, un identificateur de chaîne. Vous pouvez mapper une chaîne à un identificateur de propriété en appelant [**IPropertyStorage :: WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames). Toutefois, l’utilisation d’identificateurs de propriété est susceptible d’être beaucoup plus efficace que l’utilisation de chaînes.

Les propriétés qui sont demandées par le nom de chaîne (PRSPEC \_ LPWStr) sont mappées sans respect de la casse aux identificateurs de propriété (ID), car ils sont spécifiés dans le jeu de propriétés actuel (et en fonction des paramètres régionaux système actuels).

Lorsque le type de propriété est VT \_ LPSTR et que la propriété est lue à partir d’un jeu de propriétés ANSI, autrement dit, la page de codes pour le jeu de propriétés est définie sur une valeur autre que Unicode, la valeur de la propriété utilise la même page de codes que le jeu de propriétés. Lorsqu’une \_ propriété VT LPSTR est lue à partir d’un jeu de propriétés Unicode, la valeur de la propriété utilise la page de codes ANSI par défaut du système, autrement dit, la page de codes retournée par la fonction **GetACP** .

Un [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), à l’exception de ceux qui sont des pointeurs vers des flux et des stockages, est appelé un **PROPVARIANT** simple. Ces **PROPVARIANT** simples reçoivent des données par valeur, donc un appel à [**IPropertyStorage :: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) fournit une copie des données que l’appelant possède. Pour créer ou mettre à jour ces propriétés, appelez [**IPropertyStorage :: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple).

En revanche, les types variant VT \_ Stream, VT \_ streaming \_ Object, VT \_ Storage et VT \_ stocked \_ Object sont des propriétés non simples, car au lieu de fournir une valeur, la méthode récupère un pointeur vers l’interface indiquée, à partir de laquelle les données peuvent ensuite être lues. Ces types autorisent le stockage de grandes quantités d’informations par le biais d’une seule propriété. Il existe plusieurs problèmes qui surviennent lors de l’utilisation de propriétés qui ne sont pas simples.

Pour créer ces propriétés, comme pour les autres propriétés, appelez [**IPropertyStorage :: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Au lieu d’appeler la même méthode pour mettre à jour, toutefois, il est plus efficace d’appeler [**IPropertyStorage :: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) pour obtenir le pointeur d’interface vers le flux ou le stockage, puis d’écrire des données à l’aide des méthodes [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ou [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Un flux ou un stockage ouvert via une propriété est toujours ouvert en mode direct, donc un niveau supplémentaire de transaction imbriquée n’est pas introduit. Toutefois, il peut toujours s’agir d’une transaction sur la propriété définie dans son ensemble, en fonction de son mode d’ouverture ou de création par le biais de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage). En outre, les balises d’accès et de mode de partage spécifiées lors de l’ouverture ou de la création du jeu de propriétés sont passées aux flux de propriétés ou aux stockages.

Les durées de vie des pointeurs de stockage ou de flux basés sur des propriétés, bien que théoriquement indépendantes des pointeurs [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) et [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) associés, en fait, dépendent effectivement de ces derniers. Les données visibles via le flux ou le stockage sont liées à la transaction sur l’objet de stockage de propriétés à partir duquel elles sont récupérées, tout comme pour un objet de stockage (qui prend en charge [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)) avec un flux de données et des sous-objets de stockage contenus. Si la transaction sur l’objet parent est abandonnée, les pointeurs [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) et **IStorage** existants subordonnés à cet objet ne sont plus accessibles. Étant donné que **IPropertyStorage** est la seule interface sur l’objet de stockage de propriété, la durée de vie utile des pointeurs **IStream** et **IStorage** contenus est limitée par la durée de vie de l’interface **IPropertyStorage** .

L’implémentation doit également gérer la situation dans laquelle la même propriété de flux ou de valeur de stockage est demandée plusieurs fois via la même instance d’interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . Par exemple, dans l’implémentation du fichier composé COM, l’ouverture réussit ou échoue selon que la propriété est déjà ouverte ou non.

Un autre problème est que plusieurs s’ouvrent en mode traité. Le résultat dépend du niveau d’isolement spécifié par un appel aux méthodes [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) (méthode [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) ou [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) , via les indicateurs STGM) au moment de l’ouverture du stockage des propriétés.

Si l’appel permettant d’ouvrir le jeu de propriétés spécifie l’accès en lecture-écriture, les propriétés [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)sont toujours ouvertes avec un accès en lecture-écriture. Les données peuvent ensuite être écrites à l’aide de ces interfaces, en modifiant la valeur de la propriété, qui est la méthode la plus efficace pour mettre à jour ces propriétés. La valeur de propriété elle-même n’a pas de niveau supplémentaire d’imbrication de transactions, de sorte que les modifications sont délimitées sous la transaction (le cas échéant) sur l’objet de stockage de propriété.

## <a name="storage-and-stream-properties"></a>propriétés de Stockage et de flux

Pour écrire un flux ou un objet de stockage dans un jeu de propriétés, le jeu de propriétés doit avoir été créé comme étant insimple. pour plus d’informations sur les jeux de propriétés simple et not simple, consultez la section intitulée [Stockage et les objets de flux pour un jeu de propriétés](storage-vs--stream-for-a-property-set.md). Les types de propriétés suivants, tels qu’ils sont spécifiés dans le champ *VT* des éléments du tableau *rgvar* , sont les types de flux ou de stockage : VT \_ Stream, VT \_ Storage, VT \_ streamingd \_ Object, VT \_ stocked \_ Object.

Pour écrire un flux ou un objet de stockage en tant que propriété dans un jeu de propriétés non-simple, appelez [**IPropertyStorage :: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Bien que vous appeliez également cette méthode pour mettre à jour des propriétés simples, il ne s’agit pas d’un moyen efficace de mettre à jour les objets de flux et de stockage dans un jeu de propriétés. Cela est dû au fait que la mise à jour de l’une de ces propriétés via un appel à **WriteMultiple** crée dans l’objet de stockage des propriétés une copie des données transmises, et les pointeurs [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ne sont pas conservés au-delà de la durée de cet appel. Il est généralement plus efficace de mettre à jour les objets de flux ou de stockage directement en appelant d’abord [**IPropertyStorage :: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) pour obtenir le pointeur d’interface vers le flux ou le stockage, puis en écrivant des données via les méthodes **IStream** ou **IStorage** .

Par exemple, vous pouvez appeler [**IPropertyStorage :: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) pour écrire un flux ou un objet de stockage **null** . L’implémentation créera ensuite un objet vide dans le jeu de propriétés. Vous pouvez ensuite accéder à cet objet en appelant [**IPropertyStorage :: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple). Lorsque vous avez terminé la mise à jour de cet objet, vous n’avez pas besoin de l’écrire dans le jeu de propriétés, car vos mises à jour se trouvent directement dans le jeu de propriétés.

Un flux ou un stockage ouvert via une propriété est toujours ouvert en mode direct, donc un niveau supplémentaire de transaction imbriquée n’est pas introduit. Il peut toujours y avoir une transaction sur la propriété définie dans son ensemble. (Par exemple, si l' [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) a été obtenu en appelant [**IPropertySetStorage :: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) avec STGM \_ Indicateur traité défini dans le paramètre *grfMode* .) En outre, un flux ou un flux de données basé sur les propriétés est ouvert en mode lecture-écriture, si possible, étant donné le mode sur le jeu de propriétés ; Sinon, le mode de lecture est utilisé.

Comme mentionné précédemment, lorsqu’un objet Stream ou Storage est écrit dans une propriété définie avec la méthode [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) , une copie de l’objet est effectuée. Lorsqu’une telle copie est effectuée sur un objet de flux, l’opération de copie commence à la position de recherche actuelle de la source. La position de recherche n’est pas définie en cas d’échec, mais en cas de réussite, elle se trouve à la fin du flux. le pointeur de recherche n’est pas restauré à sa position d’origine.

Si une propriété de flux ou de stockage a été lue à partir d’un jeu de propriétés avec [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple), est toujours ouverte et un appel ultérieur à [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) pour la même propriété est effectué, l’opération **WriteMultiple** réussit. Le flux ou la propriété de stockage précédemment ouverts est placé dans l’État rétabli (tous les appels à ce dernier retourneront l' \_ erreur STG E \_ revertd Error).

Si la méthode [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) retourne une erreur lors de l’écriture d’un tableau de propriétés, ou même des propriétés individuelles non simples, la quantité de données réellement écrites n’est pas définie.

## <a name="reference-properties"></a>Propriétés de référence

Si une structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) spécifiée comprend l' \_ indicateur VT ByRef dans son membre **VT** , la propriété associée est une propriété de référence. Une propriété de référence est automatiquement déréférencée avant l’écriture de la valeur dans le jeu de propriétés. Par exemple, si le membre **VT** de la structure **PROPVARIANT** spécifie une valeur de type VT VT \_ \| VT \_ i4, la valeur réelle écrite est un \_ type VT I4. Un appel ultérieur à la méthode [**IPropertyStorage :: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) retourne une valeur en tant que VT \_ I4. L’utilisation des propriétés de référence est semblable à l’appel de la fonction [VariantCopyInd](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) . [VariantCopyInd](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) libère la variante de destination et effectue une copie de la VARIANTARG source, en effectuant l’indirection nécessaire si la source est spécifiée comme étant VT \_ ByRef. Cette fonction est utile quand une copie d’une variante est nécessaire et pour garantir qu’elle n’est pas VT \_ ByRef, par exemple lors de la gestion des arguments dans une implémentation de [**IDispatch :: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke).

## <a name="notes-to-callers"></a>Notes pour les appelants

Il est recommandé de créer les jeux de propriétés au format Unicode, en ne définissant pas l' \_ indicateur ANSI PROPSETFLAG dans le paramètre *GrfFlags* de [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Il est également recommandé d’éviter d’utiliser \_ des valeurs VT LPSTR et d’utiliser à la \_ place des valeurs VT LPWStr. Lorsque la page de codes du jeu de propriétés est Unicode, les \_ valeurs de chaîne de VT LPSTR sont converties au format Unicode lorsqu’elles sont stockées, et reviennent aux valeurs de chaîne multioctets lors de leur récupération. Lorsque la page de codes du jeu de propriétés n’est pas Unicode, les noms de propriétés, les \_ Chaînes VT BSTR et les valeurs de propriété non simples sont convertis en chaînes multioctets lorsqu’elles sont stockées, puis reconvertis en Unicode lors de leur récupération, le tout à l’aide de la page de codes ANSI du système actuelle.

## <a name="notes-to-implementers"></a>Notes pour les responsables de l’implémentation

Lors de l’allocation d’un identificateur de propriété, l’implémentation peut choisir n’importe quelle valeur qui n’est pas actuellement utilisée dans le jeu de propriétés pour un identificateur de propriété, à condition qu’il ne soit pas égal à 0 ou 1 ou supérieur à 0x80000000, qui sont toutes des valeurs réservées. Le paramètre *propidNameFirst* établit une valeur minimale pour les identificateurs de propriété dans le jeu et doit être supérieure à 1 et inférieure à 0x80000000. Consultez la section Notes ci-dessus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IPropertyStorage-implémentation de fichier composé](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[IPropertyStorage-implémentation du système de fichiers NTFS](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[IPropertyStorage-implémentation autonome](ipropertystorage-stand-alone-implementation.md)
</dt> </dl>

 

 